{{OftenUpdate}}
{{HTML}}
下表比较了[[HTML|HTML]]对一些[[排版引擎|排版引擎]]的支持与兼容性。请参阅各个产品的条目获得更多信息。除非脚注中另有规定，比较均基于稳定版本，无任何附加组件、扩展或外部程序。

本条目只考虑HTML 4与用于<code>text/html</code>的[[XHTML|XHTML]] 1.0（所谓“HTML兼容”XHTML） 。欲了解更多XHTML相关的比较，请参见[[排版引擎比较_(XHTML)|排版引擎比较 (XHTML)]]。

如给出了版本号，则说明自该版本起完全支持该特性（基于HTML 4.01）。专有扩展不包括在内。

[[W3C|W3C]]不再推荐使用的标签、属性和专有标签在[[排版引擎比较_(非标准HTML)|排版引擎比较 (非标准HTML)]]中进行了比较。

{{浏览器引擎命名}}
{{功能成熟度表格圖例}}

== 全局结构元素 ==
{| style="text-align: center; width:80%; background: #ececec" class="wikitable"
! style="width: 16em" |
! [[Trident_(排版引擎)|Trident]]
! [[Tasman|Tasman]]
! [[Gecko|Gecko]]
! [[WebKit|WebKit]]
! [[KHTML|KHTML]]
! [[Presto|Presto]]
! [[iCab|iCab]]
|-
! {{rh}} colspan="8" | 基本元素
|-
| style="text-align: left" | <tt>html</tt>
| {{IE|5.0}}
| rowspan="3" {{yes}}
| rowspan="3" {{yes|1.0}}
| rowspan="3" {{yes}}
| rowspan="3" {{yes}}
| rowspan="3" {{yes|1.0}}
| rowspan="3" {{yes}}
|-
| style="text-align: left" | <tt>head</tt>
| rowspan="2" {{IE|4.0}}
|-
| style="text-align: left" | <tt>body</tt>
|-
! {{rh}} colspan="8" | 元数据
|-
| style="text-align: left" | <tt>title</tt>
| rowspan="2" {{IE|4.0}}
| rowspan="2" {{yes}}
| rowspan="2" {{yes|1.0}}
| rowspan="2" {{yes}}
| rowspan="2" {{yes}}
| rowspan="2" {{yes|1.0}}
| rowspan="2" {{yes}}
|-
| style="text-align: left" | <tt>meta</tt>
|-
! {{rh}} colspan="8" | 标题
|-
| style="text-align: left" | <tt>h1</tt>
| rowspan="6" {{IE|4.0}}
| rowspan="6" {{yes}}
| rowspan="6" {{yes|1.0}}
| rowspan="6" {{yes}}
| rowspan="6" {{yes}}
| rowspan="6" {{yes|1.0}}
| rowspan="6" {{yes}}
|-
| style="text-align: left" | <tt>h2</tt>
|-
| style="text-align: left" | <tt>h3</tt>
|-
| style="text-align: left" | <tt>h4</tt>
|-
| style="text-align: left" | <tt>h5</tt>
|-
| style="text-align: left" | <tt>h6</tt>
|-
! {{rh}} colspan="8" | 分组元素
|-
| style="text-align: left" | <tt>div</tt>
| rowspan="2" {{IE|4.0}}
| rowspan="2" {{yes}}
| rowspan="2" {{yes|1.0}}
| rowspan="2" {{yes}}
| rowspan="2" {{yes}}
| rowspan="2" {{yes|1.0}}
| rowspan="2" {{yes}}
|-
| style="text-align: left" | <tt>span</tt>
|}

== 文本元素 ==
{| style="text-align: center; width: 80%; background: #ececec" class="wikitable"
! style="width: 16em" |
! [[Trident_(排版引擎)|Trident]]
! [[Tasman|Tasman]]
! [[Gecko|Gecko]]
! [[WebKit|WebKit]]
! [[KHTML|KHTML]]
! [[Presto|Presto]]
! [[iCab|iCab]]
|-
! {{rh}} colspan="8" | 短语
|-
| style="text-align: left" | <tt>em</tt>
| rowspan="9" {{IE|4.0}}
| rowspan="10" {{yes}}
| rowspan="10" {{yes|1.0}}
| rowspan="10" {{yes}}
| rowspan="10" {{yes}}
| rowspan="10" {{yes|1.0}}
| rowspan="10" {{yes}}
|-
| style="text-align: left" | <tt>strong</tt>
|-
| style="text-align: left" | <tt>dfn</tt>
|-
| style="text-align: left" | <tt>code</tt>
|-
| style="text-align: left" | <tt>samp</tt>
|-
| style="text-align: left" | <tt>kbd</tt>
|-
| style="text-align: left" | <tt>var</tt>
|-
| style="text-align: left" | <tt>cite</tt>
|-
| style="text-align: left" | <tt>acronym</tt>
|-
| style="text-align: left" | <tt>abbr</tt>
| {{yes|3.1}}
|-
! {{rh}} colspan="8" | 引文
|-
| style="text-align: left" | <tt>blockquote</tt>
| {{IE|4.0}}
| rowspan="2" {{yes}}
| {{yes|1.0}}
| rowspan="2" {{yes}}
| rowspan="2" {{yes}}
| rowspan="2" {{yes|1.0}}
| rowspan="2" {{yes}}
|-
| style="text-align: left" | <tt>q</tt>
| {{yes|4.0}}
| {{yes|1.8}}{{#tag:ref|<code><q></code>在Gecko 1.8之前不支持嵌套使用。<ref>{{Cite document |url=http://www.mozilla.org/projects/deerpark/new-web-dev-features.html |date= 27 May 2005 |accessdate=25 March 2011 |title=New Web Developer Features in Deer Park Alpha 1 |publisher=Mozilla}}</ref>|group=注}}
|-
! {{rh}} colspan="8" | 下标与上标
|-
| style="text-align: left" | <tt>sub</tt>
| rowspan="2" {{IE|4.0}}
| rowspan="2" {{yes}}
| rowspan="2" {{yes|1.0}}
| rowspan="2" {{yes}}
| rowspan="2" {{yes}}
| rowspan="2" {{yes|1.0}}
| rowspan="2" {{yes}}
|-
| style="text-align: left" | <tt>sup</tt>
|-
! {{rh}} colspan="8" | 行与段
|-
| style="text-align: left" | <tt>p</tt>
| rowspan="2" {{IE|4.0}}
| rowspan="3" {{yes}}
| rowspan="3" {{yes|1.0}}
| rowspan="3" {{yes}}
| rowspan="3" {{yes}}
| rowspan="3" {{yes|1.0}}
| rowspan="3" {{yes}}
|-
| style="text-align: left" | <tt>pre</tt>
|-
| style="text-align: left" | <tt>br</tt>
| {{IE|5.0}}
|-
! {{rh}} colspan="8" | 标记文档修改
|-
| style="text-align: left" | <tt>ins</tt>
| rowspan="2" {{IE|4.0}}
| rowspan="2" {{yes}}
| rowspan="2" {{yes|1.0}}
| rowspan="2" {{yes}}
| rowspan="2" {{yes}}
| rowspan="2" {{yes|1.0}}
| rowspan="2" {{yes}}
|-
| style="text-align: left" | <tt>del</tt>
|}

== 列表元素 ==
{| style="text-align: center; width: 80%; background: #ececec" class="wikitable"
! style="width: 16em" |
! [[Trident_(排版引擎)|Trident]]
! [[Tasman|Tasman]]
! [[Gecko|Gecko]]
! [[WebKit|WebKit]]
! [[KHTML|KHTML]]
! [[Presto|Presto]]
! [[iCab|iCab]]
|-
! {{rh}} colspan="8" | 无序和有序列表
|-
| style="text-align: left" | <tt>ul</tt>
| rowspan="3" {{IE|4.0}}
| rowspan="3" {{yes}}
| rowspan="3" {{yes|1.0}}
| rowspan="3" {{yes}}
| rowspan="3" {{yes}}
| rowspan="3" {{yes|1.0}}
| rowspan="3" {{yes}}
|-
| style="text-align: left" | <tt>ol</tt>
|-
| style="text-align: left" | <tt>li</tt>
|-
! {{rh}} colspan="8" | 定义列表
|-
| style="text-align: left" | <tt>dl</tt>
| rowspan="3" {{IE|4.0}}
| rowspan="3" {{yes}}
| rowspan="3" {{yes|1.0}}
| rowspan="3" {{yes}}
| rowspan="3" {{yes}}
| rowspan="3" {{yes|1.0}}
| rowspan="3" {{yes}}
|-
| style="text-align: left" | <tt>dt</tt>
|-
| style="text-align: left" | <tt>dd</tt>
|}

== 表格元素 ==
{| style="text-align: center; width: 80%" class="wikitable"
|- style="background: #ececec"
! style="width: 16em" |
! [[Trident_(排版引擎)|Trident]]
! [[Tasman|Tasman]]
! [[Gecko|Gecko]]
! [[WebKit|WebKit]]
! [[KHTML|KHTML]]
! [[Presto|Presto]]
! [[iCab|iCab]]
|-
! {{rh}} colspan="8" | 基本元素
|-
| style="text-align: left; background: #ececec" | <tt>table</tt>
| rowspan="5" {{IE|4.0}}
| rowspan="5" {{yes}}
| rowspan="5" {{yes|1.0}}
| rowspan="5" {{yes}}
| rowspan="5" {{yes}}
| rowspan="5" {{yes|1.0}}
| rowspan="5" {{yes}}
|-
| style="text-align: left; background: #ececec" | <tt>caption</tt>
|-
| style="text-align: left; background: #ececec" | <tt>tr</tt>
|-
| style="text-align: left; background: #ececec" | <tt>th</tt>
|-
| style="text-align: left; background: #ececec" | <tt>td</tt>
|-
! {{rh}} colspan="8" | 行组
|-
| style="text-align: left; background: #ececec" | <tt>thead</tt>
| rowspan="3" {{IE|4.0}}
| rowspan="3" {{yes}}
| rowspan="3" {{yes|1.0}}
| rowspan="3" {{yes}}
| rowspan="3" {{yes}}
| rowspan="3" {{yes|1.0}}
| rowspan="2" {{yes}}
|-
| style="text-align: left; background: #ececec" | <tt>tbody</tt>
|-
| style="text-align: left; background: #ececec" | <tt>tfoot</tt>
| {{Dunno}}
|-
! {{rh}} colspan="8" | 列组
|-
| style="text-align: left; background: #ececec" | <tt>colgroup</tt>
| rowspan="2" {{IE|4.0}}
| rowspan="2" {{Dunno}}
| rowspan="2" {{yes|1.0}}
| rowspan="2" {{yes}}
| rowspan="2" {{yes}}
| rowspan="2" {{yes|1.0}}
| rowspan="2" {{yes}}
|-
| style="text-align: left; background: #ececec" | <tt>col</tt>
|}

== 链接元素 ==
{| style="text-align: center; width: 80%; background: #ececec" class="wikitable"
! style="width: 16em" |
! [[Trident_(排版引擎)|Trident]]
! [[Tasman|Tasman]]
! [[Gecko|Gecko]]
! [[WebKit|WebKit]]
! [[KHTML|KHTML]]
! [[Presto|Presto]]
! [[iCab|iCab]]
|-
| style="text-align: left" | <tt>a</tt>
| rowspan="3" {{IE|4.0}}
| rowspan="3" {{yes}}
| rowspan="3" {{yes|1.0}}
| rowspan="3" {{yes}}
| rowspan="3" {{yes}}
| rowspan="3" {{yes|1.0}}
| rowspan="3" {{yes}}
|-
| style="text-align: left" | <tt>link</tt>
|-
| style="text-align: left" | <tt>base</tt>
|}

== 多媒体元素 ==
{| style="text-align: center; width: 80%; background: #ececec" class="wikitable"
! style="width: 16em" |
! [[Trident_(排版引擎)|Trident]]
! [[Tasman|Tasman]]
! [[Gecko|Gecko]]
! [[WebKit|WebKit]]
! [[KHTML|KHTML]]
! [[Presto|Presto]]
! [[iCab|iCab]]
|-
! {{rh}} colspan="8" | 图像
|-
| style="text-align: left" | <tt>img</tt>
| {{IE|4.0}}
| {{yes}}
| {{yes|1.0}}
| {{yes}}
| {{yes}}
| {{yes|1.0}}
| {{yes}}
|-
! {{rh}} colspan="8" | 一般包含
|-
| style="text-align: left" | <tt>object</tt>
| {{yes|4.0}}{{#tag:ref|对图像来说，该对象会被添加一个框架。不支持其它内容类型且作为一个ActiveX包装，该元素不会被正确实现。版本7之前不支持嵌套对象回退机制。<ref>{{Cite document |url=http://msdn.microsoft.com/library/default.asp?url=/workshop/essentials/whatsnew/whatsnew_70_sdk.asp |title=What's New in Internet Explorer 7 |publisher=Microsoft |work=[[Microsoft_Developer_Network|Microsoft Developer Network]]|accessdate=25 March 2011}}</ref>|group=注}}
| rowspan="2" {{yes}}
| rowspan="2" {{yes|1.0}}
| rowspan="2" {{yes}}
| rowspan="2" {{yes}}
| rowspan="2" {{yes|1.0}}
| rowspan="2" {{yes}}
|-
| style="text-align: left" | <tt>param</tt>
| {{IE|6.0}}
|-
! {{rh}} colspan="8" | 图像映射
|-
| style="text-align: left" | <tt>map</tt>
| {{IE|4.0}}
| rowspan="2" {{yes}}
| rowspan="2" {{yes|1.0}}
| rowspan="2" {{yes}}
| rowspan="2" {{yes}}
| rowspan="2" {{yes|1.0}}
| rowspan="2" {{yes}}
|-
| style="text-align: left" | <tt>area</tt>
| {{yes|5.0}}
|}

== 框架元素 ==
框架元素可将文档呈现于多个视图中，可以是独立窗口或子窗口。框架排版只能用于框架集配置中。所有框架在XHTML 1.1中均不可用（使用通用的对象元素代替内联框架）。
{| style="text-align: center; width: 80%; background: #ececec" class="wikitable"
! style="width: 16em" |
! [[Trident_(排版引擎)|Trident]]
! [[Tasman|Tasman]]
! [[Gecko|Gecko]]
! [[WebKit|WebKit]]
! [[KHTML|KHTML]]
! [[Presto|Presto]]
! [[iCab|iCab]]
|-
! {{rh}} colspan="8" | 框架排版
|-
| style="text-align: left" | <tt>frameset</tt>
| rowspan="3" {{IE|4.0}}
| rowspan="3" {{yes}}
| rowspan="3" {{yes|1.0}}
| rowspan="3" {{yes}}
| rowspan="3" {{yes}}
| rowspan="3" {{yes|1.0}}
| rowspan="3" {{yes}}
|-
| style="text-align: left" | <tt>frame</tt>
|-
| style="text-align: left" | <tt>noframes</tt>
|-
! {{rh}} colspan="8" | 内联框架
|-
| style="text-align: left" | <tt>iframe</tt>
| {{IE|4.0}}
| {{yes}}
| {{yes|1.0}}
| {{yes}}
| {{yes}}
| {{yes|1.0}}
| {{yes}}
|}

== 表单元素 ==
{| style="text-align: center; width: 80%" class="wikitable"
! style="width: 16em" |
! [[Trident_(排版引擎)|Trident]]
! [[Tasman|Tasman]]
! [[Gecko|Gecko]]
! [[WebKit|WebKit]]
! [[KHTML|KHTML]]
! [[Presto|Presto]]
! [[iCab|iCab]]
|-
! {{rh}} colspan="8" | 基本结构
|-
| style="text-align: left; background: #ececec" | <tt>form</tt>
| rowspan="3" {{IE|4.0}}
| rowspan="3" {{yes}}
| rowspan="3" {{yes|1.0}}
| rowspan="3" {{yes}}
| rowspan="3" {{yes}}
| rowspan="3" {{yes|1.0}}
| rowspan="3" {{yes}}
|-
| style="text-align: left; background: #ececec" | <tt>fieldset</tt>
|-
| style="text-align: left; background: #ececec" | <tt>legend</tt>
|-
! {{rh}} colspan="8" | 表单控件和标签
|-
| style="text-align: left; background: #ececec" | <tt>button</tt>
| {{IE|4.0}}{{#tag:ref|在Internet Explorer 8.0（trident 4.0）之前和早期的兼容模式下，innerText属性会代替值属性提交。<ref>{{cite web|title=button element {{!}} button object (Internet Explorer)|url=http://msdn.microsoft.com/en-us/library/ms535211|publisher=Microsoft|accessdate=29 November 2012}}</ref>|group=注}}
| rowspan="4" {{yes}}
| rowspan="4" {{yes|1.0}}
| rowspan="4" {{yes}}
| rowspan="3" {{yes}}
| rowspan="4" {{yes|1.0}}
| rowspan="4" {{yes}}
|-
| style="text-align: left; background: #ececec" | <tt>textarea</tt>
| rowspan="3" {{IE|4.0}}
|-
| style="text-align: left; background: #ececec" | <tt>input</tt>
|-
| style="text-align: left; background: #ececec" | <tt>label</tt>
| {{yes|3.4.2}}
|-
! {{rh}} colspan="8" | 列表框（组合框）
|-
| style="text-align: left; background: #ececec" | <tt>select</tt>
| rowspan="3" {{IE|4.0}}
| rowspan="3" {{yes}}
| rowspan="3" {{yes|1.0}}
| rowspan="3" {{yes}}
| rowspan="3" {{yes}}
| rowspan="3" {{yes|1.0}}
| rowspan="3" {{yes}}
|-
| style="text-align: left; background: #ececec" | <tt>optgroup</tt>
|-
| style="text-align: left; background: #ececec" | <tt>option</tt>
|}

== 表现元素 ==
尽管并非所有的表现元素都不被推荐使用，但使用这些元素不利于样式表的发展。 不被推荐使用的元素在严格配置与XHTML 1.1下被禁止。
{| style="text-align: center; width: 80%; background: #ececec" class="wikitable"
! style="width: 16em" |
! [[Trident_(排版引擎)|Trident]]
! [[Tasman|Tasman]]
! [[Gecko|Gecko]]
! [[WebKit|WebKit]]
! [[KHTML|KHTML]]
! [[Presto|Presto]]
! [[iCab|iCab]]
|-
! {{rh}} colspan="8" | 字体风格
|-
| style="text-align: left" | <tt>b</tt>
| rowspan="5" {{IE|4.0}}
| rowspan="5" {{yes}}
| rowspan="5" {{yes|1.0}}
| rowspan="5" {{yes}}
| rowspan="5" {{yes}}
| rowspan="5" {{yes|1.0}}
| rowspan="5" {{yes}}
|-
| style="text-align: left" | <tt>i</tt>
|-
| style="text-align: left" | <tt>big</tt>
|-
| style="text-align: left" | <tt>small</tt>
|-
| style="text-align: left" | <tt>tt</tt>
|-
! {{rh}} colspan="8" | 水平线
|-
| style="text-align: left" | <tt>hr</tt>
| {{IE|4.0}}
| {{yes}}
| {{yes|1.0}}
| {{yes}}
| {{yes}}
| {{yes|1.0}}
| {{yes}}
|}

== 样式表元素 ==
{| style="text-align: center; width: 80%" class="wikitable"
|- style="background: #ececec"
! style="width: 16em" |
! [[Trident_(排版引擎)|Trident]]
! [[Tasman|Tasman]]
! [[Gecko|Gecko]]
! [[WebKit|WebKit]]
! [[KHTML|KHTML]]
! [[Presto|Presto]]
! [[iCab|iCab]]
|-
| style="text-align: left; background: #ececec" | <code><link rel="style" … /></code>
| {{IE|4.0}}
| rowspan="2" {{yes}}
| rowspan="2" {{yes|1.0}}
| rowspan="2" {{yes}}
| rowspan="2" {{yes}}
| rowspan="2" {{yes|1.0}}
| rowspan="2" {{yes}}
|-
| style="text-align: left; background: #ececec" | <code>style</code>
| {{yes|6.0}}{{#tag:ref|Internet Explorer 9（Trident 5.0)与更早的版本<code><style></code>元素受到限制。<ref>{{Cite document |url=http://support.microsoft.com/kb/262161 |title=A webpage that uses CSS styles does not render correctly in Internet Explorer |publisher=Microsoft|accessdate=25 March 2011|date=31 August 2010}}</ref><ref>{{cite |url=http://msdn.microsoft.com/en-US/library/ie/hh920762 |title=Removal of style sheet limits (Windows) |publisher=Microsoft}}</ref>|group=注}}
|}

== 脚本元素 ==
用于嵌入客户端脚本（[[JavaScript|JavaScript]]）的元素。
{| style="text-align: center; width: 80%" class="wikitable"
! style="width: 16em" |
! [[Trident_(排版引擎)|Trident]]
! [[Tasman|Tasman]]
! [[Gecko|Gecko]]
! [[WebKit|WebKit]]
! [[KHTML|KHTML]]
! [[Presto|Presto]]
! [[iCab|iCab]]
|-
| style="text-align: left; background: #ececec" | <tt>script</tt>
| {{IE|5.0}}
| rowspan="2" {{yes}}
| rowspan="2" {{yes|1.0}}
| rowspan="2" {{yes}}
| rowspan="2" {{yes}}
| rowspan="2" {{yes|1.0}}
| rowspan="2" {{yes}}
|-
| style="text-align: left; background: #ececec" | <tt>noscript</tt>
| {{incorrect}}
|}

== 语言元素 ==
{| style="text-align: center; width: 80%" class="wikitable"
! style="width: 16em" |
! [[Trident_(排版引擎)|Trident]]
! [[Tasman|Tasman]]
! [[Gecko|Gecko]]
! [[WebKit|WebKit]]
! [[KHTML|KHTML]]
! [[Presto|Presto]]
! [[iCab|iCab]]
|-
| style="text-align: left; background: #ececec" | <tt>bdo</tt>
| {{IE|5.0}}
| {{Dunno}}
| {{yes|1.0}}
| {{yes}}
| {{partial}}
| {{yes|1.0}}
| {{Dunno}}
|}

== 通用属性 ==
{| style="text-align: center; width: 80%" class="wikitable"
! style="width: 16em" |
! [[Trident_(排版引擎)|Trident]]
! [[Tasman|Tasman]]
! [[Gecko|Gecko]]
! [[WebKit|WebKit]]
! [[KHTML|KHTML]]
! [[Presto|Presto]]
! [[iCab|iCab]]
|-
! {{rh}} colspan="8" | 元素标识符
|-
| style="text-align: left; background: #ececec" | <tt>id</tt>
| rowspan="2" {{IE|3.0}}
| rowspan="2" {{yes}}
| rowspan="2" {{yes|1.0}}
| rowspan="2" {{yes}}
| rowspan="2" {{yes}}
| rowspan="2" {{yes|1.0}}
| rowspan="2" {{yes}}
|-
| style="text-align: left; background: #ececec" | <tt>class</tt>
|-
! {{rh}} colspan="8" | 内嵌样式
|-
| style="text-align: left; background: #ececec" | <tt>style</tt>
| {{IE|3.0}}
| {{yes}}
| {{yes|1.0}}
| {{yes}}
| {{yes}}
| {{yes|1.0}}
| {{yes}}
|-
! {{rh}} colspan="8" | 公告信息
|-
| style="text-align: left; background: #ececec" | <tt>title</tt>
| {{IE|4.0}}
| {{yes}}
| {{yes|1.0}}
| {{yes}}
| {{yes}}
| {{yes|1.0}}
| {{yes}}
|-
! {{rh}} colspan="8" | 语言信息
|-
| style="text-align: left; background: #ececec" | <tt>lang</tt>
| {{IE|4.0}}
| rowspan="2" {{yes}}
| rowspan="2" {{yes|1.0}}
| rowspan="2" {{yes}}
| rowspan="2" {{yes}}
| rowspan="2" {{yes|1.0}}
| rowspan="2" {{yes}}
|-
| style="text-align: left; background: #ececec" | <tt>dir</tt>
| {{IE|5.0}}
|}

==注释==
{{Reflist | group=注}}

==参考资料==
{{Reflist}}
{{Refbegin}}
* {{cite web | work=Microsoft Developer Network|publisher=Microsoft|title=CSS Enhancements in Internet Explorer 6 | url=http://msdn.microsoft.com/library/default.asp?url=/library/en-us/dnie60/html/cssenhancements.asp | accessdate=25 March 2011|date=September 2006}}
* {{cite web | title=Mozilla Developer Documentation | work=Mozilla's DOCTYPE sniffing | url=http://www.mozilla.org/docs/web-developer/quirks/doctypes.html |accessdate=25 March 2011}}
* {{cite web | publisher=Opera Software|title=HTML, XHTML, and WML support in Opera Presto 2.6|url=http://www.opera.com/docs/specs/html/ |accessdate=25 March 2011}}
{{Refend}}

==外部链接==
* {{en}}[http://webref.info/?ID=1 webref.info的HTML参考]
* {{en}}[http://hsivonen.iki.fi/doctype/ 使用DOCTYPE声明激活正确的排版模式]
* {{en}}[http://gutfeldt.ch/matthias/articles/doctypeswitch/table.html 文档类型和它们各自的排版模式]
* {{en}}[http://www.blooberry.com/indexdot/html/supportkey/a.htm HTML支持历史]
* {{en}}[http://www.webdevout.net/browser_support_html.php 网页浏览器HTML支持]
* {{en}}[http://caniuse.com/ Can I Use]——展示各大浏览器对HTML5、CSS3的支持程度。
* {{en}}[http://html5test.com/ HTML5test]——测试各大浏览器对HTML5的支持程度。
* {{en}}[https://developer.mozilla.org/en-US/docs/Web/HTML Mozilla Developer Network上面的HTML相关资料]

{{Layout engines}}

[[Category:HTML|Category:HTML]]
[[Category:排版引擎比较|Category:排版引擎比较]]