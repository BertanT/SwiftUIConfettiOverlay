# SwiftUI ConfettiOverlay
## 👀 Overview
Simple and Customizable SwiftUI Confetti Modifier Package That Lets You Add Confetti to Anything!

**Requires macOS 12, iOS/iPadOS 15, tvOS 15, or watchOS 8 or newer. Built for SwiftUI.**
## 🚀 Usage
Add the `.confettiOverlay` modifier to any SwiftUI view you want to add confetti over, and that's it! 
The below example demonstrates how to add confetti to a View and toggle the emission with a Button. A boolean `State` property controls the emission.

```swift
struct ContentView: View {
    // Property controlling emission
    @State private var isEmitting = false
    
    var body: some View {
        VStack {
            Button("Party!") {
                // Toggle emission on button press
                isEmitting.toggle()
            }
        }
        // Add confetti over this VStack! 🎉
        .confettiOverlay(isEmitting: isEmitting)
    }
}
```
### Customization
```swift
.confettiOverlay(amount: Float, colors: [UIColor], isEmitting: Bool)
```
You can also play with these optional parameters and make the confetti your own!
* **`amount`**: `Float` value to control how much confetti you want!
  * Default: `10`
* **`colors`**: `UIColor` `Array` value that specifies the colors of your confetti pieces. Add as many as you wish! 
  * Default: `[.systemYellow, .systemMint, .systemIndigo, .systemPink]`

