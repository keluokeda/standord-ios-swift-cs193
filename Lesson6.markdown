### Gestures
给一个view添加手势
```swift
@IBOutlet weak var pannableView: UIView {
      didSet {
          let panGestureRecognizer = UIPanGestureRecognizer(
              target: self, action: #selector(ViewController.pan(recognizer:))
)
          pannableView.addGestureRecognizer(panGestureRecognizer)
      }
}
```
