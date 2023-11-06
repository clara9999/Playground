<h1>HW2</h1>
    
```swift
import SwiftUI

    struct ContentView: View {
        @State private var choiceIndex: Int = 0
        private let choices = ["剪刀", "石頭", "布"]
        
        var body: some View {
            VStack {
                Text(choices[choiceIndex])
                    .padding()
                    .font(.largeTitle)
                
                Button("GO!") {
                    choiceIndex = Int.random(in: 0...2)
                }
                .padding()
                .frame(width: 200, height: 60)
                .background(Color.pink)
                .foregroundColor(.white)
                .cornerRadius(15)
            }
        }
    }
```
<img width="40%"  src="https://github.com/clara9999/Playground/blob/main/IMG_0397.jpeg">
