### 如何使用AutoLayout

### Range
代码
```swift
for i in stride(from: 0.5, to: 1.5, by: 0.2) {
    print(i)
}
```
输出
```
0.5
0.7
0.9
1.1
1.3
```

### Tuples
- 一组数据

代码
```swift
let x :(name:String,age:Int) = ("hankuke",10)
print("name is \(x.name) ,age is \(x.age)")
```
输入
```
name is hankuke ,age is 10
```

### Computed Properties
- 计算属性，和存储属性（Store Properties）不同的是，计算属性并不存在于宿主之上，仅仅在设置的时候改变一些东西或者在取的时候返回一些值。
- 许多时候我们需要一个可以被推到出的属性，而不需要一个存储属性
```swift
 private var lastChooseIndex : Int?{
        get{
            var foundIndex:Int?
            
            for index in cards.indices {
                if cards[index].isFaceUp {
                    if foundIndex == nil {
                        foundIndex = index
                    }else{
                        return nil
                    }
                }
            }
            
            return foundIndex
        }
        set{
            for index in cards.indices {
                cards[index].isFaceUp = (index == newValue)
            }
        }
    }
```

### Access Control 
#### 访问控制
- internal
- privalte 
- private(set)
- fileprivate
- public
- open

### Extensions
- 给一个类增加属性和方法
```swift
extension Int {
    var random : Int{
        if self > 0 {
            return Int(arc4random_uniform(UInt32(self)))
        } else if self < 0 {
            return -Int(arc4random_uniform(UInt32(abs(self))))
        }else {
            return 0
        }
    }
}
```

### enum
- 枚举是值类型
- 每个状态可以有属于自己的数据组合
```swift
enum Food {
    case drink
    case cookie(String,String,Int)
    case fries
    case hamburger(price:Double)
}
```
- 设置枚举的值
```swift
let f1 = Food.drink
let f2 = Food.hamburger(price: 20.1)
let f3 :Food = .cookie("0", "1", 2)
```

- 访问枚举的数据
 ```swift
 switch f1 {
        case .drink:
            print("dirnk")
        case .hamburger(let price):
            print("hamburger price = \(price)")
        default:
            print("error")
        }
 ```
 - 枚举可以有方法，但不能有存储属性
 - 如果有个方法需要改变自身，需要用**mutating**关键字
 ```swift
 enum Food {
    case drink
    case cookie(String,String,Int)
    case fries
    case hamburger(price:Double)
    
    mutating func toCookie(){
        self = .cookie("T", "1", 2)
    }
}
```


