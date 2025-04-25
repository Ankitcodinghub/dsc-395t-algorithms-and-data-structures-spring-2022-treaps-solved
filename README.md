# dsc-395t-algorithms-and-data-structures-spring-2022-treaps-solved



**<span style='color:red'>TO GET THIS SOLUTION VISIT:</span>** https://www.ankitcodinghub.com/product/dsc-395t-algorithms-and-data-structures-spring-2022-treaps-solved/

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;104788&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;DSC 395T Algorithms and Data Structures — Spring 2022 Treaps Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">
            
<div class="kksr-stars">
    
<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">
            

<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">
            

<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">
            

<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">
            

<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">
            

<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
    
<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">
            

<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">
            

<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">
            

<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">
            

<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">
            

<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>
                

<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (1 vote)    </div>
    </div>
In this assignment you will implement a map (associative lookup) using a data structure called a treap, which is a combination of a tree and a heap. Your key challenge in this assignment will be to carefully and thoroughly test your data structure, so you should also design a testing program for your code. For this assignment, you should not discuss testing strategies with other teams.

1 Treaps

A treap is a binary search tree that uses randomization to produce balanced trees. In addition to holding a key-value pair (a map entry), each node of a treap holds a randomly chosen priority value, such that the priority values satisfy the heap property: Each node other than the root has a priority that is at least as large as the priorities of its two children. An example treap is shown in Figure 1, where the keys are shown at the top of each node and the priorities are shown at the bottom of each node. Notice that the keys obey the binary search tree (BST) property and the priorities obey the heap property. Because the keys obey the BST property, a lookup operation can be performed just as with any BST. However, the insert and remove operations are slightly more complex.

Figure 1: A treap for a map with key set {1, 3, 4, 5, 6, 8, 9}. For each node, the key is shown in the top half, while the priority is shown in the bottom half. The priority values are chosen at random, with larger numbers representing higher priorities. The values are not shown.

To remove a node x, we “reverse” the insertion. We rotate x down the treap until it becomes a leaf, and then we simply clip it off. At each step, the decision to rotate left or right is governed by the relative priorities of the children. The child with the higher priority should become the new parent. Thus, if x’s left child has higher priority than x’s right child, then we rotate right around x. Conversely, if x’s right child has higher priority than x’s left child, then we rotate left around x. Figure 3 illustrates a removal requiring 2 rotations. This removal reverses the insertion of Figure 2.

All three map operations—lookup, insert, and remove—run in time O(h), where h is the height of the treap. It is not hard to show that a treap with n nodes has expected height Θ(log n). Note that the root of a treap is determined by

1

44743873366940344075105991936248631 Figure 2: Inserting new node x into a treap. (a) The new node x, with key k=4 and priority p=4743, is added as a leaf according to the BST property. The heap property with respect to x’s parent y is violated. (b) The situation after a right rotation around y; the heap property with respect to x’s new parent z is violated. (c) After a left rotation around z, the heap property is restored.

the randomly chosen priorities. The node with the highest priority is the root. Thus, the root node is equally likely to contain any of the map entries, regardless of the order in which the entries are inserted or removed. Consequently, we expect that half of the entries will be in the left subtreap and the other half in the right subtreap. The analysis of treap height is therefore similar to the analysis of recursion depth in quicksort.

2 Your Assignment

Implement a map using a treap. In particular, you should implement the following abstract base class. Your treap should store entries with keys that are Comparable objects and values that are any object. In both cases the Treap is generic on the exact type; keys have type KT and values have type VT. The lookup(k) method should return None if no entry with key k is in the map.

class Treap(ABC, Generic[KT, VT], Iterable): def get_root_node(self) -&gt; TreapNode: … def lookup(self, key: KT) -&gt; Optional[VT]: … def insert(self, key: KT, value: VT) -&gt; None: … def remove(self, key: KT) -&gt; Optional[VT]: … def split(self, threshold: KT) -&gt; “List[Treap[KT, VT]]”: … def join(self, other: “Treap[KT, VT]”) -&gt; None: … def meld(self, other: “Treap[KT, VT]”) -&gt; None: … def difference(self, other: “Treap[KT, VT]”) -&gt; None: … def balance_factor(self) -&gt; float: … def __str__(self) -&gt; str: … def __iter__(self) -&gt; Iterator: …

A more detailed description of the interface is in treap.py. Implement your treap-based map as TreapMap in treap map.py and make sure your implementation inherits from Treap[KT, VT]. Please use the TreapNode deﬁned in treap node.py and do not modify or rename the six existing ﬁelds in TreapNode. You only need to modify treap map.py for this assignment, but you are welcome to modify treap node.py as well.

The insert method. two nodes will never have an equal priority, which is enforced by the starter code.

Insertion into the treap should be implemented as outlined in Figure 2. You can assume that

2

873361059569403248610599193616940324864743919361694034407510599193624863187336344073440787336447435yx4yxxzz(c)(a)(b)47434 Figure 3: Removing a node x from a treap. (a) Node x has two children, of which the left child z has higher priority. (b) After a right rotation around x, node x now has only one child, y. (c) After a left rotation around x, node x is now a leaf and can be clipped off like an excessively long toenail.

The remove method. Removal from the treap should be implemented as outlined in Figure 3.

The split method. A treap T can be split, using a key k, to produce two treaps, T1 and T2, such that T1 contains all of the entries in T with key less than k, and T2 contains all of the entries in T with key greater than or equal to k. To perform the split, we insert into T a new entry x with key k and priority p =MAX PRIORITY, forming a new treap T (cid:48). (MAX PRIORITY is deﬁned by the Treap abstract base class.) Because x has the highest possible priority, x is the root of T (cid:48), so the split has been accomplished with T1 being the left subtreap and T2 being the right subtreap. You should not “lose” any value associated with k if k is already in the treap, although it is ok if you destroy the old treap.

The join method. The inverse of a split is join, in which two treaps, T1 and T2, with all keys in T1 being smaller than all keys in T2, are merged to form a new treap T . To perform the join, we create a new treap T (cid:48) with an arbitrary new root node x and with T1 and T2 as the left and right subtreaps. We then remove x from T (cid:48) to form the joined result T .

Split and join both take time O(h), where h is the height of the T (the input to split or the result of join). The expected height is Θ(log n), where n is the size of T , so split and join both run in O(log n) expected time. More interestingly, split and join can be used as subroutines to meld two treaps or take the difference between two treaps. Those functions are described in the Karma section.

3 Testing

4 Karma

Three of the operations in the interface (balance factor(), meld() and difference()) are optional. Im- plement them for extra karma. If you do not implement them, raise an AttributeError.

3

8733610595(c)(a)(b)694034407510599193624863144743xz694032486474391936134407873364yxz694032486105991936187336344075yx44743 4.1 Meld

A meld takes two treaps, T1 and T2 and merges them into a new treap T , much like the Vulcan mind meld for which it is named1. Unlike a join, a meld does not require any relationship between the keys in T1 and T2. Meld is a naturally recursive procedure and should be able to meld two treaps of size n and m (m ≤ n) in O(m log(n/m)) time. Describe how you meld treaps and how your algorithm meets the speciﬁed asymptotic time bound.

4.2 Difference

The difference between two treaps, T1 and T2, is a treap T containing the keys of T1 with any keys in T2 removed. The difference can also be computed recursively and also runs in O(m log(n/m)) time. Describe how you take a difference and how your algorithm satisﬁes this time bound.

4.3 Diagnosing Problems Through Testing

Typically, the goal of a test program is to identify bugs. With some additional work, you can attempt to diagnose common problems by observing the behavior of the program. For example, if the iterator misses one key, it is likely that the missing key is the ﬁrst or last key added. A test program can attempt to verify this hypothesis and provide a suggestion to the user. Can you use your test program to assist in ﬁnding common mistakes?

4.4 Balance Statistics

It would be useful to know how balanced or imbalanced your treap is. The balance factor is the ratio between the height of the treap and the minimum possible height. A perfectly balanced treap will have a balance factor of 1.0. Include observations on how well the treap seems to keep itself balanced in your report.

5 What to Turn in

Submit a single ZIP ﬁle containing your report and code. Make sure your code is packaged in a directory named py treaps.

Acknowledgments. We thank Bobby Blumofe for the original version of this assignment, and we thank Walter Chang, Arthur Peters, and Ashlie Martinez for their subsequent modiﬁcations.

1Not really.

4
