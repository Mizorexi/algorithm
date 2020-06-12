## 文档定义
``` c++
template<class InputIterator, class UnaryPredicate>
bool all_of(
    InputIterator first,
    InputIterator last,
    UnaryPredicate pred);

template <class ExecutionPolicy, class ForwardIterator, class UnaryPredicate>
bool all_of(
    ExecutionPolicy&& exec,
    ForwardIterator first,
    ForwardIterator last,
    UnaryPredicate pred);
```
#### 参数
    1.exec 执行策略
    2.first,last 指定范围的首位迭代器
    3.pred 判断的条件,这是一个用户定义的检查元素是否满足条件的谓词对象.一个一元谓词采用一个参数,返回true or false.
    
#### 返回值
    若指定范围内的每一个元素都满足用户指定的条件，或者范围是empty,返回true;否则返回false.
