### struct
- 值类型
- copy on write
- 如果一个方法要改变自身的属性，需要在该方法上加上**mutating**
- 没有继承
- 通过**let**控制可变性（例如使用let声明的数据就不可编辑）
- 支持函数式编程

### protocol
- 只有方法声明

### Function Types
```swift
var operation : (Double) -> Double
operation = { -$0 }
let result  = operation(20.0)
```
