### Thrown Errors
声明一个可能会抛出错误的方法
```swift
func save() throws -> String {
        return ""
    }
```
有三种方法可以调用可能会抛出错误的方法
- 捕获错误
```swift
do {
            try save()
        } catch let error {
//            error.localizedDescription
        }
```
- 强制执行，如果有错误就直接崩溃
```swift
let s = try! save()
```
- 可选执行，如果出现错误返回String?
```swift
let s = try? save()
```
