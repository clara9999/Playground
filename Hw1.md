<h1>HW1</h1>
    
```swift
import SwiftUI

struct ContentView: View {
    var body: some View {
            Image("D")
            .resizable()
            .scaledToFit()
            .overlay(Image(systemName: "car")
                .font(.system(size:30))
                .foregroundColor(.yellow)
                .shadow(color: .gray, radius:5, x: 5, y: 0)
                 .frame(maxWidth: .infinity, maxHeight: .infinity, alignment: .topTrailing)
            )
                
        
            .overlay(
                Text("我的Mbti : ISTJ")
                    .fontWeight(.heavy)
                    .lineSpacing(2)
                    .font(.system(size: 20))
                    .foregroundColor(.yellow)
                    .frame(width: 230, height:50, alignment: .center)
                    .background(Color.pink)
                    .cornerRadius(10)
                    .opacity(0.8)
                ,
                alignment: .bottom
            )
            .overlay(
                Text("1091545 曹晴榆")
                    .fontWeight(.light)
                    .lineSpacing(2)
                    .font(.system(size: 30))
                    .foregroundColor(.yellow)
                    .opacity(1)
                ,
                alignment: .top
            )
    }
}


```
<img width="40%"  src="https://github.com/clara9999/Playground/blob/8516822ead2e817e577c2e6ad15348a399aa9735/IMG_0365.jpeg">
