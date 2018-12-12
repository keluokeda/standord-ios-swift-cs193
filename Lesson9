### ViewController Lifecycle
```swift
import UIKit

class BaseViewController: UIViewController {
    
   

    override func viewDidLoad() {
        super.viewDidLoad()
        printMessage("viewDidLoad")
        
        // Do any additional setup after loading the view.
    }
    
    override func viewWillAppear(_ animated: Bool) {
        super.viewWillAppear(animated)
        
        printMessage("viewWillAppear \(animated)")
    }
    
    override func viewDidAppear(_ animated: Bool) {
        super.viewDidAppear(animated)
        
        printMessage("viewDidAppear \(animated)")
    }
    
    override func viewWillLayoutSubviews() {
        super.viewWillLayoutSubviews()
        printMessage("viewWillLayoutSubviews")
    }
    
    override func viewDidLayoutSubviews() {
        super.viewDidLayoutSubviews()
        printMessage("viewDidLayoutSubviews")
    }
    
    override func viewWillDisappear(_ animated: Bool) {
        super.viewWillDisappear(animated)
        printMessage("viewWillDisappear \(animated)")
    }
    
    override func viewDidDisappear(_ animated: Bool) {
        super.viewDidDisappear(animated)
        printMessage("viewDidDisappear \(animated)")

    }
    
    deinit {
        printMessage("deinit")
    }
    
    var controllerName:String{
        return "nil"
    }

   

    
    private func printMessage(_ message : String){
        print("\(controllerName) \(message)")
    }
}
```
输出信息
```
master viewDidLoad
master viewWillAppear false
master viewWillLayoutSubviews
master viewDidLayoutSubviews
master viewDidAppear false
detail viewDidLoad
master viewWillDisappear true
detail viewWillAppear true
detail viewWillLayoutSubviews
detail viewDidLayoutSubviews
master viewDidDisappear true
detail viewDidAppear true
detail viewWillDisappear true
master viewWillAppear true
detail viewDidDisappear true
master viewDidAppear true
detail deinit
```
