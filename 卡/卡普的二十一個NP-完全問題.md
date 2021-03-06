在[[計算複雜度理論|計算複雜度理論]]內，一個極度重要的成就是[[史提芬·古克|史提芬·古克]]在1971年證明出了第一個[[NP-完全|NP-完全]]問題— [[布爾可滿足性問題|布爾可滿足性問題]]。<ref>{{cite book|author = [[Stephen_Cook|Stephen Cook]]|year = 1971|chapter = [http://portal.acm.org/citation.cfm?coll=GUIDE&dl=GUIDE&id=805047 The Complexity of Theorem Proving Procedures]|title = Proceedings of the third annual ACM symposium on Theory of computing|pages = 151–158}}</ref>在1972年，[[理查德·卡普|理查德·卡普]]將這個想法往前推進，發表了他著名的論文"'''Reducibility Among Combinatorial Problems'''"，其內證明了21個不同的，均因為其難解而惡名昭彰的[[組合數學|組合數學]]與[[圖論|圖論]]問題，是NP-完全問題。<ref>{{cite book | author = Richard M. Karp | chapter = [http://www.cs.berkeley.edu/~luca/cs172/karp.pdf Reducibility Among Combinatorial Problems] | title = Complexity of Computer Computations | editor = R. E. Miller and J. W. Thatcher (editors) | publisher = New York: Plenum | pages = 85–103 | year = 1972}}</ref>

藉由展示出許多研究上面重要的問題是NP-完全問題，卡普促進了研究[[NP_(複雜度)|NP]]，NP-完備性，以及現在著名的[[P/NP問題|P = NP]]這些問題。

==問題==

卡普的21個問題列表如下。下列问题加上了缩进排版，以表示出這些問題歸約的方向。例如，[[精确覆盖问题|精确覆盖问题]]可以歸約到[[背包問題|背包問題]]（Knapsack），因此背包問題是NP-完全問題。

* [[布爾可滿足性問題|布爾可滿足性問題]]（Satisfiability）：對於布爾邏輯內[[合取範式|合取範式]]方程式的滿足性問題（一般直接叫做SAT）
** [[線性規劃#.E6.95.B4.E6.95.B8.E8.A6.8F.E5.8A.83|0-1整數規劃]]（0-1 integer programming）
** [[分團問題|分團問題]]（Clique，參考[[獨立集|獨立集]]）
*** [[Set_packing|Set packing]]（Set packing）
*** [[覆蓋_(圖論)|最小顶点覆盖问题]]（Vertex cover）
**** [[集合覆盖问题|集合覆盖问题]]（Set covering）
**** [[Feedback_vertex_set|Feedback node set]]（Feedback node set）
**** [[Feedback_arc_set|Feedback arc set]]
**** [[哈密頓路徑問題|有向哈密頓迴圈]]（卡普命名，现称Directed Hamiltonian cycle）
***** [[哈密頓路徑問題|無向哈密頓迴圈]]（卡普命名，现称Undirected Hamiltonian cycle）
** 每句话至多3个变量的[[布爾可滿足性問題|布爾可滿足性問題]]（Satisfiability with at most 3 literals per clause, 3-SAT）
*** [[图着色问题|图着色问题]]（Chromatic number）
**** [[分團覆蓋問題|分團覆蓋問題]]（Clique cover）
**** [[精確覆蓋問題|精確覆蓋問題]]（Exact cover）
***** [[Hitting_set|Hitting set]]（Hitting set）
***** [[Steiner_tree|Steiner tree]]（Steiner tree）
***** [[三维匹配问题|三维匹配问题]]（3-dimensional matching）
***** [[背包問題|背包問題]]（Knapsack）
****** [[Job_sequencing|Job sequencing]]（Job sequencing）
****** [[划分问题|划分问题]]（Partition）
******* [[最大割問題|最大割問題]]（Max cut）

== 參考資料 ==
<references/>
[[Category:NP完全問題|*]]
[[Category:數學列表|Category:數學列表]]