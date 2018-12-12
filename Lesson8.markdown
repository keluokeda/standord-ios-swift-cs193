三种动画
- UIViewPropertyAnimator
- Transitions
- Dynamic Animator

动画可以影响的view属性
- frame/center
- bounds
- transform
- alpha
- backgroundColor

### UIViewPropertyAnimator
示例代码
```swift
@IBAction func click1(_ sender: Any) {
        UIViewPropertyAnimator
            .runningPropertyAnimator(
                withDuration: 3.0,
                delay: 5.0,
                options: [.curveEaseInOut],
                animations: {
                    print("start animation")
                    self.label.alpha = 0.0
                })
        { (position) in
            print("completion \(position)")
            self.label.alpha = 1.0
        }
    }
```
参数含义
- withDuration：表示动画持续的时间。
- delay：动画延迟时间。
- options：选项。
- animations：希望view变成什么状态，立刻执行，无视delay。
- completion：动画结束时的回调。

### Transitions
实例代码
```swift
UIView.transition(
            with: label,
            duration: 1.0,
            options: [.transitionFlipFromLeft],
            animations: {
                print("animations")
            })
        { (finish) in
            print("finish = \(finish)")
        }
```



参数含义
- with：动画作用的对象。
- duration：动画时长。
- 
