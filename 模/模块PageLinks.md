local ToolbarBuilder = require('Module:Toolbar')

local p = {} -- Page object
local trackingCategories = {} -- Table for storing the tracking categories.
local demo

-- Define a custom error message for this module.
local function err(msg, section)
	local help
	if section then
		help = ' ([[Template:Page-multi#'_.._section_.._'|帮助]])'
	else
		help = ''
	end
	local cat
	if demo == 'yes' then
		cat = ''
	else
		cat = '[[Category:有错误的PageLinks嵌入|Category:有错误的PageLinks嵌入]]'
	end
	return '<span class="error">[[Template:Page-multi|Page-multi]]出错：' .. msg 
        .. help .. '.</span>' .. cat
end

----------------------------------------------------------------------------------------------
--      To add more link types, write a function that produces an individual link, and put  --
--      it at the bottom of the list below. Then, add a link code for your function to the  --
--      "linktypes" table. Try and make the code three letters or less. 
--
--      If you want more helper strings, you can define them in the generatePageDataStrings --
--      function below.                                                                     --
----------------------------------------------------------------------------------------------

----------------------------------------------------------------------------------------------
--                                LINK FUNCTIONS START                                      --
----------------------------------------------------------------------------------------------

local function makePageLink()
	return p.fullText and '[[:'_.._p.fullText_.._'|' .. p.fullText .. ']]' or ''
end

local function makeTalkLink()
	return '[['_.._tostring(p.talkPageTitle)_.._'|讨论]]'
end

local function makeWhatLinksHereLink()
	return '[[Special:WhatLinksHere/'_.._p.fullText_.._'|-{zh-hans:链接; zh-hant:連結;}-]]'
end

local function makeRelatedChangesLink()
	return '[[Special:RelatedChanges/'_.._p.fullText_.._'|相关]]'
end

local function makeEditLink()
	local url = p:fullUrl( 'action=edit' );
	return '[' .. url .. ' 编辑]'
end

local function makeHistoryLink()
	local url = p:fullUrl( 'action=history' );
	return '[' .. url .. ' 历史]'
end

local function makeWatchLink()
	local url = p:fullUrl( 'action=watch' );
	return '[' .. url .. ' 监视]'
end

local function makeTargetLogsLink()
	local url = mw.uri.fullUrl( 'Special:Log', 'page=' .. mw.uri.encode(p.fullText) )
	return '[' .. tostring(url) .. ' 日志]'
end

local function makeEditFilterLogLink()
	local url = mw.uri.fullUrl( 'Special:AbuseLog', 'wpSearchTitle=' .. mw.uri.encode(p.fullText) )
	return '[' .. tostring(url) .. ' 编辑过滤器日志]'
end

local function StatsGrokSeURL(year, month, lang)
	local url = 'http://stats.grok.se/' .. lang .. '/' .. year .. string.format("%0.2d",month) .. '/' .. mw.uri.encode( p.fullText )
	return url
end

local function monthsago(months)
	local rv = os.date("*t")
	if rv.month < months + 1 then
		rv.month = 12 + (rv.month - months)
		rv.year = rv.year - 1
	else
		rv.month = rv.month - months
	end

	return rv
end

local function makeViewsLastMonthStatsGrokSeLink()
	local when = monthsago(1)
	return '[' .. StatsGrokSeURL(when.year, when.month, 'en') .. ' 统计]'
end

----------------------------------------------------------------------------------------------
--                                   LINK FUNCTIONS END                                     --
--      To enable new link functions, add the code to the "linktypes" table directly below. --
----------------------------------------------------------------------------------------------

local linktypes = {
    {'t'   , makeTalkLink},
    {'wlh' , makeWhatLinksHereLink},
    {'rc'  , makeRelatedChangesLink},
    {'edit', makeEditLink},
    {'h'   , makeHistoryLink},
    {'w'   , makeWatchLink},
    {'tl'  , makeTargetLogsLink},
    {'efl' , makeEditFilterLogLink},
    {'vlm-sgs' , makeViewsLastMonthStatsGrokSeLink},
}

local function getLink(linktype)
    local linkNumber
    for i, value in ipairs(linktypes) do
        if value[1] == linktype then
            linkNumber = i
            break
        end
    end
    if not linkNumber then
        return err('“' .. linktype .. '”不是有效的链接代码', '非有效链接代码')
    end
    local result = linktypes[linkNumber][2]()
    if type(result) ~= 'string' then
        return err(
            '代码“' .. linktype .. '”的函数没有返回字符串值',
            '函数未返回字符串值'
        )
    end
    return result
end

local function makeToolbar(args)
    local targs = {}
    local numArgsExist = false
    for k, v in pairs(args) do
        if type(k) == 'number' and p then
            numArgsExist = true
            targs[k] = getLink(v)
        end
    end
    targs.style = args.small and 'font-size: 90%;'
    targs.separator = args.separator or 'dot'
    
    if numArgsExist == false then
        return nil -- Don't return a toolbar if no numeric arguments exist. -- this bit looks odd
    else
        return ToolbarBuilder.main(targs)
    end
end

local function generatePageDataStrings(args)
    -- If the page name is absent or blank, return an error and a tracking category.
    if args.page == '' or not args.page then
        return err('没有探测到页面')
    end
    local noError
    noError, p = pcall(mw.title.new, args.page)
    if not noError then
    	return err('pcall mw.title 失败')
	end
	if args.exists and (not p or p['id'] == 0) then
    	return err('未找到页面')
    end
end

local function generateTrackingCategories()
    if demo == 'yes' then
        return ''
    else
        return table.concat(trackingCategories)
    end
end

-- This function generates a table of all available link types, with their previews.
-- It is used in the module documentation.
local function getLinkTable(args)
    demo = args.demo -- Set the demo variable.
    -- Generate the page data strings and return any errors.
    local dataStringError = generatePageDataStrings(args)
    if dataStringError then
        return dataStringError
    end
    
    -- Build a table of all of the links.
    local result = '<table class="wikitable plainlinks sortable">'
        .. '\n<tr><th>代码</th><th>预览</th></tr>'
    for i, value in ipairs(linktypes) do
        local code = value[1]
        result = result .. "\n<tr><td>'''" .. code .. "'''</td><td>" .. getLink(code) .. '</td></tr>'
    end
    result = result .. '\n</table>'
    
    return result
end

local function getSingleLink(args)
    demo = args.demo -- Set the demo variable.
    -- Generate the page data strings and return any errors.
    local dataStringError = generatePageDataStrings(args)
    if dataStringError then
        return dataStringError
    end
    
    local linktype = args[1]
    if not linktype then 
        return err('没有指定链接类型')
    end
    local result = getLink(linktype)
    result = result .. generateTrackingCategories()
    return result
end

local function getLinksToolbar(args)
    demo = args.demo -- Set the demo variable.
    -- Generate the page data strings and return any errors.
    local dataStringError = generatePageDataStrings(args)
    if dataStringError then
        return dataStringError
    end    
    
    -- Build the template output.
    local result = makeToolbar(args) -- Get the toolbar contents.
    result = (result or '') .. generateTrackingCategories()
    return result
end

local function getLinks(args)
	local result = getLinksToolbar(args)

	if result then
		if args.sup then
			result = '<sup>' .. result .. '</sup>'
		end
		result = ' ' .. result
	else
		result = '' -- If there are no links specified, don't return the toolbar at all.
	end
	if args.nopage then
		result = '<span>' .. result .. '</span>'
	else
		if p then
			result = '<span>' .. makePageLink() .. result .. '</span>'
		else
			result = '<span>[['_.._args.page_.._'|' .. args.page .. ']]' .. result .. '</span>'
		end
	end

	return result
end

local function getExampleLinks(args)
    -- This function enables example output without having to specify any
    -- parameters to #invoke.
    args.demo = 'yes'
    args.page = 'Example'
    return getLinks(args)
end

local function makeWrapper(func)
    return function (frame)
        -- If called via #invoke, use the args passed into the invoking template.
        -- Otherwise, for testing purposes, assume args are being passed directly in.
        local origArgs
        if frame == mw.getCurrentFrame() then
            origArgs = frame:getParent().args
            for k, v in pairs(frame.args) do
                origArgs = frame.args
                break
            end
        else
            origArgs = frame
        end
 
        -- Strip whitespace, and treat blank arguments as nil.
        -- 'page', and 'separator' have different behaviour depending on
        -- whether they are blank or nil, so keep them as they are.
        local args = {}
        for k, v in pairs(origArgs) do
            v = mw.text.trim(v)
            if v ~= '' or k == 'page' or k == 'separator' then
                args[k] = v
            end
        end
    
        return func(args)
    end
end

return {
    main = makeWrapper(getLinks),
    single = makeWrapper(getSingleLink),
    toolbar = makeWrapper(getLinksToolbar),
    linktable = makeWrapper(getLinkTable),
    example = makeWrapper(getExampleLinks)
}