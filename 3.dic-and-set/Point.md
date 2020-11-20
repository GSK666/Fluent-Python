# 第3章 字典和集合
## 重点
1. 字典dic
2. 字典推导
3. 常见的映射方法
4. setdefault处理
5. 映射的弹性键查询，defaultdic，特殊方法__missing__，
6. 字典的变种，collections.OrderedDic在添加键的时候会保持顺序，collections.ChainMap可以容纳数个不同的映射对象，collections.Counter会给键准备一个计数器，每次更新一个键的时候会增加这个计数器，collections.UserDcit让用户继承写子类的
7. 不可变映射类型，MappingProxyType
8. 集合，结合基础的中缀运算符
9. 集合推导
10. 集合的操作
11. 对于查询，集合的速度最快，字典其次，列表最慢
12. 字典中的散列表，为了获取 my_dict[search_key] 背后的值，Python首先会调用hash(search_key) 来计算search_key的散列值，把这个值最低的几位数字当作偏移量，在散列表里查找表元(具体取几位，得看当前散列表的大小)。若找到的表元是空的，则抛出KeyError异常。若不是空的，则表元里会有一对found_key:found_value，Python会检验search_key == found_key是否为真，如果它们相等的话，就会返回found_value，如果search_key和found_key不匹配的话，这种情况称为散列冲突
13. 在插入新值时，Python 可能会按照散列表的拥挤程度来决定是 否要重新分配内存为它扩容。如果增加了散列表的大小，那散列值 所占的位数和用作索引的位数都会随之增加，这样做的目的是为了 减少发生散列冲突的概率
14. 键必须是可散列的，字典在内存上的开销巨大，键的查询很快，键的次序取决于添加顺序，往字典里添加新键可能会改变已有键的顺序，集合相似