相同层级diff

步骤
1. 对新集合节点进行循环，通过唯一`key`可以判断新老集合中是否存在相同的节点

2. 如果存在相同节点，进行移动操作

3. 移动前需要对当前节点在老集合的位置与`lastIndex`进行比较，`if(child._mountIndex<lastIndex)`则进行移动操作

4. 当完成新集合中所有节点 diff 时，最后还需要对老集合进行循环遍历，判断是否存在新集合中没有但老集合中仍存在的节点，发现存在这样的节点 D，因此删除节点 D，到此 diff 全部完成