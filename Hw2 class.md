<h1>HW2 CLASS</h1>
    
```swift
import SwiftUI

struct ContentView: View {
    @State var count:Int = 0
    var body: some View{
        VStack{
            Text(String(count))
                .padding(.all,10)
                .frame(width: 150, height: 120, alignment:.center)
                .font(.system(size:100))
            Button(action: {
                count+=1
            }, label:{
                Text("Add")
                    .padding(.all,10)
                    .frame(width: 300, height: 100, alignment: .center)
                    .font(.system(size: 50))
                    .background(Color.purple)       
                    .foregroundColor(.white)
                    .border(Color.purple, width: 5)
                    .cornerRadius(20)
    })
            Button(action: {
                count-=1
            }, label:{
                Text("Subtract")
                    .padding(.all,10)
                    .frame(width: 300, height: 100, alignment: .center)
                    .font(.system(size: 50))
                    .background(Color.purple)       
                    .foregroundColor(.white)
                    .border(Color.purple, width: 5)
                    .cornerRadius(20)
            })
                                }}}
    
```
