# SwiftLibrary
Here you can find swift examples.

## Add buttons above keyboard

Add this into your `viewDidLoad()` - best way.

```Swift
let bar = UIToolbar()
let uiBarItem1 = UIBarButtonItem(title: "Encode", style: .plain, target: self, action: #selector(buttonTapped))
let uiBarItem2 = UIBarButtonItem(title: "Encode", style: .plain, target: self, action: #selector(buttonTapped))

bar.items = [uiBarItem1, uiBarItem2]
bar.sizeToFit()
yourCustomTextView.inputAccessoryView = bar
```

Create `buttonTapped()` function.

```Swift
@objc func encodeTapped(_ sender: UIBarButtonItem) {
  print("Hello World!")
}
```

## Hide keyboard by tapping anywhere on the screen

Add this into your `ViewController` class.
```Swift
override func touchesBegan(_ touches: Set<UITouch>, with event: UIEvent?) {
  view.endEditing(true)
}
```

