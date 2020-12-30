# SFSymbolsFinder

SFSymbolsFinder is a convenient library to get whole list of available latest SF Symbols image

## Introduction
 
 SFSymbolsFinder introduces 19 SF Symbols categories, each category represented by an `enum`: 

- `Communication`
- `Weather`
- `ObjectsAndTools`
- `Devices`
- `Connectivity`
- `Transportation`
- `Human`
- `Nature`
- `Editing`
- `Text Formatting`
- `Media`
- `Keyboard`
- `Commerce`
- `Time`
- `Health`
- `Shapes`
- `Arrows`
- `Indices`
- `Math`

All categories is based on official Apple SF Symbols application [sfsymbols](https://developer.apple.com/sf-symbols/)

## Usage

### General Usage

Use it easily with calling the enum for each category

```swift
import SFSymbolsFinder
import SwiftUI

struct ContentView: View {
  var body: some View {
    VLayout {
        // Approach 1 by using Image directly
        VLayout {
            Communication.micSlashFill.image
                                .resizable
        }
        // Approach 2 by using the system name string
        VLayout {
            Image(systemName: Communication.micSlashFill.systemName)
                                .resizable
        }
    }
  }
}
```

There are some categories that need special way to retrieve the symbols: 

### ObjectAndTools

For one of the icon which is `oneMagnifyingglass` is used for getting `1.magnifyingglass` system name

### Indices

For indices there are special ways to get 3 special symbols which is for retrieving `Currency`, `Alphabet`, and `Number`.

- For number, it supports generic type
```swift
// With Int
Indices.Number.circle(number: 1).systemName
// With String
Indices.Number.circle(number: 01).systemName
```
Please beware not every number or string is supported, in case we put 999 or "-123" it won't return anything.

- For `Alphabet`, it supports by passing `Character` enum. It supports `a` to `z`.

- For `Currency`, it supports by passing `AvailableCurrency` enum.

## Installation

SFSymbolsFinder is distributed using the [Swift Package Manager](https://swift.org/package-manager). To install it into a project, follow [this tutorial](https://developer.apple.com/documentation/swift_packages/adding_package_dependencies_to_your_app) and use this repository URL: `https://github.com/abadikaka/SFSymbolsFinder.git`.

## Credits

SFSymbolsFinder was built by [Michael Abadi S.](https://twitter.com/michaelabadiii) as a component of some of his project described in [his website](https://michaelabadi.com).

## Contributions and Support

All users are welcome and encouraged to become active participants in the project continued development — by fixing any bug that they encounter, or by improving the documentation wherever it’s found to be lacking, and adding more or missing available SF Symbols, or even only adding a Unit Test.

If you'd like to make a change, please [open a Pull Request](https://github.com/zntfdr/AStack/pull/new), even if it just contains a draft of the changes you’re planning, or a test that reproduces an issue.

If you'd like to open an issue, please submit new issue.

## Todo

- [] Add generic validation for system name

Thank you and please enjoy using **SFSymbolsFinder**!
