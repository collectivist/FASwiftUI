# FASwiftUI

Easily integrate FontAwesome 6 into your SwiftUI projects. Use Font Awesome icons as text in your SwiftUI views. Supports FontAwesome Pro or Free.

(Does not currently support the Duotone style.)

### Installation - Swift Package Manager
----------------------------------
1. Add the Swift package to your Xcode project
    1. File -> Swift Packages -> Add Package Dependency
    2. Enter https://github.com/mattmaddux/FASwiftUI.git
2. Download Font Awesome
    1. Go to https://fontawesome.com/download
    2. Download the Pro or Free version
3. Drag the following files from the download to your project:
    * /metadata/icon-families.json
    * /otfs/Font Awesome 6 Brands-Regular-400.otf
    * /otfs/Font Awesome 6 Pro-Light-300.otf (Pro Only)
    * /otfs/Font Awesome 6 [Pro/Free]-Regular-400.otf
    * /otfs/Font Awesome 6 [Pro/Free]-Solid-900.otf
    * /otfs/Font Awesome 6 Pro-Thin-100.otf (Pro Only)
    * /otfs/Font Awesome 6 Sharp-Light-300.otf (Pro Only)
    * /otfs/Font Awesome 6 Sharp-Regular-400.otf (Pro Only)
    * /otfs/Font Awesome 6 Sharp-Solid-900.otf (Pro Only)
4. Add files to target - For each of the files in the last step:
    1. Select the file in Project Navigator
    2. Open the Inspectors bar on the right and select the file inspector (first tab)
    3. Under Target Membership select each target you need to use FASwiftUI
5. Add Fonts to Info.plist
    1. Open your project's info.plist
    2. Right-Click in a blank area and choose "Add Row"
    3. Name the new entry "Fonts provided by application"
    4. Expand the entry by clicking the triangle to the left
    5. Add a new entry for each of the "otf" files you added to your project, using the full filename including the extension
6. You're done!


### Usage
----------------------------------
Use a Font Awesome icon in any view:
```swift
import SwiftUI
import FASwiftUI

struct ContentView: View {
    var body: some View {
        FAText(iconName: "bomb", size: 200)
    }
}
```

![Regualr Icon Screenshot](https://raw.githubusercontent.com/mattmaddux/FASwiftUI/master/icon-regular.png)

You can also choose an alternate style.
(This is ignored if the icon is a brand and currently duotone is not supported and will default back to regular.)

```swift
import SwiftUI
import FASwiftUI

struct ContentView: View {
    var body: some View {
        FAText(iconName: "bomb", size: 200, style: .solid)
    }
}
```

![Regualr Icon Screenshot](https://raw.githubusercontent.com/mattmaddux/FASwiftUI/master/icon-fill.png)

Set the color as you would any text.

```swift
import SwiftUI
import FASwiftUI

struct ContentView: View {
    var body: some View {
        FAText(iconName: "bomb", size: 200)
            .foregroundColor(Color.red)
    }
}
```

![Regualr Icon Screenshot](https://raw.githubusercontent.com/mattmaddux/FASwiftUI/master/icon-red.png)
