# SwiftUI ConfettiOverlay
## 👀 Overview
Simple and Customizable SwiftUI Confetti Modifier Package That Lets You Add Confetti to Anything!

**Requires Mac Catalyst 15, iOS/iPadOS 15, tvOS 15, or newer. Built for SwiftUI.**

![Static Badge](https://img.shields.io/badge/Platforms-Mac_Catalyst_15%2B_%7C_iOS_15%2B_%7C_tvOS_15%2B-F05138?logo=swift&labelColor=white)
![Static Badge](https://img.shields.io/badge/SwiftUI-3.0%2B-2a60de?logo=swift&logoColor=2a60de&labelColor=white)
## 🚀 Usage
Add the `.confettiOverlay` modifier to any SwiftUI view you want to add confetti over, and that's it! 
The below example demonstrates how to add confetti to a View and toggle the emission with a Button. A boolean `State` property controls the emission.

```swift
import SwiftUIConfettiOverlay

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

