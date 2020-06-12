## 文档定义
```c++
template<class ForwardIterator>
ForwardIterator adjacent_find(
    ForwardIterator first,
    ForwardIterator last);

template<class ForwardIterator , class BinaryPredicate>
ForwardIterator adjacent_find(
    ForwardIterator first,
    ForwardIterator last,
    BinaryPredicate pred);

template<class ExecutionPolicy, class ForwardIterator>
ForwardIterator adjacent_find(
    ExecutionPolicy&& exec,
    ForwardIterator first,
    ForwardIterator last);

template<class ExecutionPolicy, class ForwardIterator, class BinaryPredicate>
ForwardIterator adjacent_find(
    ExecutionPolicy&& exec,
    ForwardIterator first,
    ForwardIterator last,
    BinaryPredicate pred);
```
#### 参数分析
    1.exec 使用的执行策略
    2.first，last 声明查询范围的头尾迭代器
    3.pred 给出查询范围内相邻元素应该满足的条件的二进制谓词
    
#### 返回值
    若找到两个彼此相等的相邻元素或者满足二进制谓词所给定条件的相邻元素，返回第一个元素的forwarditerator
    否则返回指向last的迭代器
    
#### 注释
adjacent_find函数是一个 __非变异序列函数__ [nonmutating sequence algorithm.](啥玩意？).所给出的范围必须是有效的;所有的指针必须是可以解引用的,并且last所指定位置必须可以从first递增访问到;函数时间复杂度与范围的元素数量成线性关系。
        
