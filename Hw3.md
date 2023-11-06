<h1>HW3</h1>
    
```swift
import SwiftUI
struct ContentView: View {
    // Define the fruits
    let fruits = ["寶寶兔丸", "熊&兔丸", "貪吃兔丸", "溫泉老闆", "超人兔丸", "鳳梨兔丸", "棒球選手", "滑板選手", "桌球選手"]
    
    // Define the grid layout
    let columns: [GridItem] = Array(repeating: .init(.flexible()), count: 3)
    
    var body: some View {
        ScrollView {
            VStack{
                TitleView()
                LazyVGrid(columns: columns, spacing: 20) {
                    ForEach(fruits, id: \.self) { fruit in
                        FruitView(imageName: fruit)
                    }
                    ExpirationView2()
                }
                
                ZStack {
                    FishView()
                    ExpirationView()
                }
            }
            .padding() // Add padding around the VStack content
        }
    }
}

struct TitleView: View {
    var body: some View {
        VStack(alignment: .center, spacing: 2) {
            Text("Clara的").font(.system(size: 30))
            Text("兔丸").font(.title).foregroundColor(Color .yellow)
        }
    }
}

struct FruitView: View {
    var imageName: String
    var body: some View {
        VStack {
            Image(imageName)
                .resizable()
                .scaledToFit()
                .frame(minWidth: 0, maxWidth: .infinity, minHeight: 100, idealHeight: 100, maxHeight: .infinity, alignment: .center)
            Text(imageName.capitalized)
                .fontWeight(.bold)
                .font(.system(size: 25))
        }
    }
}

struct FishView: View {
    var body: some View {
        VStack {
            Image("貓咪兔丸")
                .resizable()
                .scaledToFit()
                .padding(.all, 15)
            Text("貓咪兔丸")
                .fontWeight(.bold)
                .font(.system(size: 30))
        }
    }
}

struct ExpirationView: View {
    var body: some View {
        Text("保存期限:♾️")
            .font(.system(size: 20))
            .foregroundColor(.yellow)
            .padding(.all,5)
            .background(Color.black)
            .opacity(0.7)
            .offset(x: 70, y: 10)
    }
}
struct ExpirationView2: View {
    var body: some View {
        Text("うさまる")
            .font(.system(size: 20))
            .foregroundColor(Color.yellow)
            .padding(.all,9)
            .background(Color.black)
            .opacity(0.7)
            .lineLimit(1)
            .offset(x: 120, y: 10)
    }
}


struct ContentView_Previews: PreviewProvider {
    static var previews: some View {
        ContentView()
    }
}

```
