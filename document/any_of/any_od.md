## 文档定义
``` c++
template<class InputIterator, class UnaryPredicate>
bool any_of(
    InputIterator first,
    InputIterator last,
    UnaryPredicate pred);

template <class ExecutionPolicy, class ForwardIterator, class UnaryPredicate>
bool any_of(
    ExecutionPolicy&& exec,
    ForwardIterator first,
    ForwardIterator last,
    UnaryPredicate pred);
```

#### 参数分析
    1.exec 执行策略
    2.last,first 确定范围的首尾迭代器
    3.pred 二进制谓词
    
#### 返回值
    若给定范围内有至少一个元素满足条件，返回true;否则返回false
