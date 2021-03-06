{{C++ Standard library}}

[[C++程序设计语言|C++程序设计语言]]中，'''<code>unordered_map</code>'''、'''<code>unordered_multimap</code>'''、'''<code>unordered_set</code>'''、'''<code>unordered_multiset</code>'''是[[标准模板库|标准模板库]]（STL）提供的一类'''无序关联容器'''（unordered associative containers）。是通过[[哈希表|哈希表]]实现的[[数据结构|数据结构]]。无序是指元素的名字（或者键值）的存储是无序的；这与用[[平衡二叉树|平衡二叉树]]实现的元素名字是有序存储的“[[关联数组|关联容器]]”是相对概念。
==历史==
[[Silicon_Graphics|SGI]]的[[标准模板库|STL]]提供了<code>hash_map</code>, <code>hash_set</code>, <code>hash_multimap</code>, <code>hash_multiset</code>等类模板。<ref>{{cite web |url= http://www.sgi.com/tech/stl/hash_map.html |title=hash_map<Key, Data, HashFcn, EqualKey, Alloc> |publisher=[[Silicon_Graphics|SGI]] |accessdate=26 January 2011}}</ref>由于其有用性，很快其它的C++编译器也支持了这一特性，如[[GNU_Compiler_Collection|GCC]]、 [[libstdc++|libstdc++]]<ref>{{cite web |url=http://gcc.gnu.org/onlinedocs/libstdc++/libstdc++-html-USERS-4.1/class____gnu__cxx_1_1hash__map.html |title=libstdc++: hash_map Class Template Reference |accessdate=26 January 2011}}</ref> 以及[[Visual_C++|MSVC]] （在stdext[[命名空间|命名空间]]）。

[[C++_Technical_Report_1|C++ TR1]]语言标准中提出了增加<code>hash_*</code>类模板<ref>{{cite web |title=A Proposal to Add Hash Tables to the Standard Library (revision 4) |author=WG21 |date=9 April 2003 |url=http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2003/n1456.html |id=n1456}}</ref>，最终接受为<code>unordered_*</code>。 <ref name="n3126">{{citation|url=http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2010/n3126.pdf |title=Working Draft, Standard for Programming Language C++ |author=WG21 |date=21 August 2010 |id=n3126}}</ref> [[Boost_C++_Libraries|Boost C++ Libraries]]也提供了一种实现。<code><boost/unordered_map.hpp></code>.<ref>{{cite web |publisher=Boost |title=Class template unordered_map |url=http://www.boost.org/doc/libs/1_45_0/doc/html/boost/unordered_map.html |accessdate=26 January 2011}}</ref>

==类成员函数==

头文件<code><unordered_map></code>中定义了类模板<code>unordered_map</code>。并满足[http://www.sgi.com/tech/stl/Container.html 容器][[concept_(generic_programming)|概念]]，这意味着它支持<code>begin()</code>、<code>end()</code>、<code>size()</code>、<code>max_size()</code>、<code>empty()</code>、 <code>swap()</code>等方法。 

{| class="wikitable" style="font-size:0.85em"
|-
!
! <code>unordered_set</code><br>([[C++11|C++11]])
! <code>unordered_map</code><br>([[C++11|C++11]])
! <code>unordered_multiset</code><br>([[C++11|C++11]])
! <code>unordered_multimap</code><br>([[C++11|C++11]])
! 描述
|-
! rowspan=4 |
| [http://en.cppreference.com/w/cpp/container/unordered_set/unordered_set (constructor)]
| [http://en.cppreference.com/w/cpp/container/unordered_map/unordered_map (constructor)]
| [http://en.cppreference.com/w/cpp/container/unordered_multiset/unordered_multiset (constructor)]
| [http://en.cppreference.com/w/cpp/container/unordered_multimap/unordered_multimap (constructor)]
| 构造函数包括缺省构造、拷贝构造、移动构造等
|-
| [http://en.cppreference.com/w/cpp/container/unordered_set/~unordered_set (destructor)]
| [http://en.cppreference.com/w/cpp/container/unordered_map/~unordered_map (destructor)]
| [http://en.cppreference.com/w/cpp/container/unordered_multiset/~unordered_multiset (destructor)]
| [http://en.cppreference.com/w/cpp/container/unordered_multimap/~unordered_multimap (destructor)]
| 析构函数
|-
| <code>[http://en.cppreference.com/w/cpp/container/unordered_set/operator=%20 operator=]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_map/operator=%20 operator=]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_multiset/operator=%20 operator=]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_multimap/operator=%20 operator=]</code>
| 赋值运算符
|-
| <code>[http://en.cppreference.com/w/cpp/container/unordered_set/get_allocator get_allocator]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_map/get_allocator get_allocator]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_multiset/get_allocator get_allocator]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_multimap/get_allocator get_allocator]</code>
| 返回分配器，用于给容器元素分配内存
|-
! rowspan=2 | Element access
| {{n/a}}
| <code>[http://en.cppreference.com/w/cpp/container/unordered_map/at at]</code>
| {{n/a}}
| {{n/a}}
| 带边界检查的返回元素（[[C++11|C++11]]）
|-
| {{n/a}}
| <code>[http://en.cppreference.com/w/cpp/container/unordered_map/operator_at operator<nowiki>[]</nowiki>]</code>
| {{n/a}}
| {{n/a}}
| 不带边界检查的返回元素，可用于插入元素
|-
! rowspan=2 | Iterators
| <code>[http://en.cppreference.com/w/cpp/container/unordered_set/begin begin,cbegin]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_map/begin begin,cbegin]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_multiset/begin begin,cbegin]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_multimap/begin begin,cbegin]</code>
| 返回指向哈希表指定条目（bucket）所包含的首元素的迭代器 （[[C++11|C++11]]）
|-
| <code>[http://en.cppreference.com/w/cpp/container/unordered_set/end end]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_map/end end]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_multiset/end end]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_multimap/end end]</code>
| 指向容器末尾的迭代器
|-
! rowspan=3 | Capacity
| <code>[http://en.cppreference.com/w/cpp/container/unordered_set/empty empty]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_map/empty empty]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_multiset/empty empty]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_multimap/empty empty]</code>
| 检查容器是否为空
|-
| <code>[http://en.cppreference.com/w/cpp/container/unordered_set/size size]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_map/size size]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_multiset/size size]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_multimap/size size]</code>
| 返回容器元素的数量。
|-
| <code>[http://en.cppreference.com/w/cpp/container/unordered_set/max_size max_size]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_map/max_size max_size]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_multiset/max_size max_size]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_multimap/max_size max_size]</code>
| 返回受系统与库的实现所限，容器元素的最大可能数量
|-
! rowspan=7 | Modifiers
| <code>[http://en.cppreference.com/w/cpp/container/unordered_set/clear clear]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_map/clear clear]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_multiset/clear clear]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_multimap/clear clear]</code>
| 清空容器
|-
| <code>[http://en.cppreference.com/w/cpp/container/unordered_set/insert insert]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_map/insert insert]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_multiset/insert insert]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_multimap/insert insert]</code>
| 插入元素
|-
| <code>[http://en.cppreference.com/w/cpp/container/unordered_set/emplace emplace]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_map/emplace emplace]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_multiset/emplace emplace]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_multimap/emplace emplace]</code>
| 原位构造 ([[C++11|C++11]])
|-
| <code>[http://en.cppreference.com/w/cpp/container/unordered_set/emplace_hint emplace_hint]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_map/emplace_hint emplace_hint]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_multiset/emplace_hint emplace_hint]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_multimap/emplace_hint emplace_hint]</code>
| 使用hint原位构造 ([[C++11|C++11]])
|-
| <code>[http://en.cppreference.com/w/cpp/container/unordered_set/try_emplace try_emplace]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_map/try_emplace try_emplace]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_multiset/try_emplace try_emplace]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_multimap/try_emplace try_emplace]</code>
| 如果给定的key在容器中不存在，原位构造一个元素 ([[C++17|C++17]])
|-
| <code>[http://en.cppreference.com/w/cpp/container/unordered_set/erase erase]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_map/erase erase]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_multiset/erase erase]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_multimap/erase erase]</code>
| 擦除元素
|-
| <code>[http://en.cppreference.com/w/cpp/container/unordered_set/swap swap]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_map/swap swap]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_multiset/swap swap]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_multimap/swap swap]</code>
| 两个容器交换内容
|-
! rowspan=4 | Lookup
| <code>[http://en.cppreference.com/w/cpp/container/unordered_set/count count]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_map/count count]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_multiset/count count]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_multimap/count count]</code>
| 返回匹配指定键值的元素数量
|-
| <code>[http://en.cppreference.com/w/cpp/container/unordered_set/find find]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_map/find find]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_multiset/find find]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_multimap/find find]</code>
| 发现具有指定键值的元素
|-
| <code>[http://en.cppreference.com/w/cpp/container/unordered_set/equal_range equal_range]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_map/equal_range equal_range]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_multiset/equal_range equal_range]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_multimap/equal_range equal_range]</code>
| 返回匹配指定键值的元素范围
|-
| <code>[http://en.cppreference.com/w/cpp/container/unordered_set/reserve reserve]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_map/reserve  reserve]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_multiset/reserve reserve]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_multimap/reserve reserve]</code>
| 扩展容器的容量（[[C++11|C++11]]）
|-
| Bucket接口
| <code>[http://en.cppreference.com/w/cpp/container/unordered_set/bucket_size bucket_size]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_map/bucket_size bucket_size]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_multiset/bucket_size bucket_size]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_multimap/bucket_size bucket_size]</code>
| 返回指定索引的哈希表条目所容纳的容器元素的数量（[[C++11|C++11]]）
|-
! rowspan=9 | 哈希策略 
|-
| <code>[http://en.cppreference.com/w/cpp/container/unordered_set/hash_function hash_function]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_map/hash_function hash_function]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_multiset/hash_function hash_function]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_multimap/hash_function hash_function]</code>
| 返回用于创制键值hash的函数对象
|-
| <code>[http://en.cppreference.com/w/cpp/container/unordered_set/key_eq key_eq]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_map/key_eq key_eq]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_multiset/key_eq key_eq]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_multimap/key_eq key_eq]</code>
| 返回键值比较函数对象（[[C++11|C++11]]）
|-
| <code>[http://en.cppreference.com/w/cpp/container/unordered_set/rehash rehash]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_map/rehash rehash]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_multiset/rehash rehash]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_multimap/rehash rehash]</code>
| 设定哈希表的条目（bucket）数量并重新生成哈希表（[[C++11|C++11]]）
|-
| <code>[http://en.cppreference.com/w/cpp/container/unordered_set/max_load_factor max_load_factor]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_map/max_load_factor max_load_factor]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_multiset/max_load_factor max_load_factor]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_multimap/max_load_factor max_load_factor]</code>
| 返回或者设置哈希表的每个条目能容纳的容器元素的最大数量（[[C++11|C++11]]）
|-
| <code>[http://en.cppreference.com/w/cpp/container/unordered_set/load_factor load_factor]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_map/load_factor load_factor]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_multiset/load_factor load_factor]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_multimap/load_factor load_factor]</code>
| 返回哈希表的每个条目容纳的容器元素的平均数量（[[C++11|C++11]]）
|-
| <code>[http://en.cppreference.com/w/cpp/container/unordered_set/max_bucket_count max_bucket_count]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_map/max_bucket_count max_bucket_count]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_multiset/max_bucket_count max_bucket_count]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_multimap/max_bucket_count max_bucket_count]</code>
| 返回由于系统及库的实现所能支持的哈希表条目的最大可能数量（[[C++11|C++11]]）
|-
| <code>[http://en.cppreference.com/w/cpp/container/unordered_set/bucket_count bucket_count]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_map/bucket_count bucket_count]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_multiset/bucket_count bucket_count]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_multimap/bucket_count bucket_count]</code>
| 返回容器中的哈希表条目的数量（[[C++11|C++11]]）
|-
| <code>[http://en.cppreference.com/w/cpp/container/unordered_set/bucket bucket]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_map/bucket bucket]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_multiset/bucket bucket]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_multimap/bucket bucket]</code>
| 返回指定键值所匹配的哈希表条目的索引（[[C++11|C++11]]）
|-
| Observers
| <code>[http://en.cppreference.com/w/cpp/container/unordered_set/operator_cmp operator==,!=]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_map/operator_cmp operator==,!=]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_multiset/operator_cmp operator==,!=]</code>
| <code>[http://en.cppreference.com/w/cpp/container/unordered_multimap/operator_cmp operator==,!=]</code>
| 两个容器的内容是否相同
|}

==例子==
<source lang="cpp">
#include <iostream>
#include <string>
#include <unordered_map>
 
int main()
{
    std::unordered_map<std::string, int> months;
    months["january"] = 31;
    months["february"] = 28;
    months["march"] = 31;
    months["april"] = 30;
    months["may"] = 31;
    months["june"] = 30;
    months["july"] = 31;
    months["august"] = 31;
    months["september"] = 30;
    months["october"] = 31;
    months["november"] = 30;
    months["december"] = 31;
    std::cout << "september -> " << months["september"] << std::endl;
    std::cout << "april     -> " << months["april"] << std::endl;
    std::cout << "december  -> " << months["december"] << std::endl;
    std::cout << "february  -> " << months["february"] << std::endl;

    //判断map中是否包含一个键值，没有直接做此事的成员函数。类似其他的STL容器，解决办法是：
    if( months.find("no_value") == months.end() )
    {
          printf("No such key in the map.");
    }
    return 0;
}
</source>

==定制哈希函数==
定制的哈希函数的参数为到定制类型的const引用，返回类型为size_t
<source lang="cpp">
struct X{int i,j,k;};

struct hash_X{
  size_t operator()(const X &x) const{
    return hash<int>()(x.i) ^ hash<int>()(x.j) ^ hash<int>()(x.k);
  }
};
</source>

定制哈希函数作为std::unordered_map的模板参数使用。
<source lang="cpp"> std::unordered_map<X,int,hash_X> my_map;</source>

或者通过特化std::hash来使用。
<source lang="cpp">
namespace std {
    template <>
        class hash<X>{
        public :
        size_t operator()(const X &x ) const{
            return hash<int>()(x.i) ^ hash<int>()(x.j) ^ hash<int>()(x.k);
        }
    };
}

//...
 std::unordered_map<X,int> my_map;
</source>

==参考文献==
{{reflist}} 
[[Category:C++標準函式庫|Category:C++標準函式庫]]