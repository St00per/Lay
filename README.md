# Lay
A library to compute a perfectly balanced collection of CGSize elements for a specified width. This project is heavily inspired by [this article](https://medium.com/@jtreitz/the-algorithm-for-a-perfectly-balanced-photo-gallery-914c94a5d8af#.ac11ixwdn) written by [Johannes Treitz](https://medium.com/@jtreitz).

<img src="docs/Screenshot@2x.jpg" width="375">

## Usage

```swift
import Lay

let sizes: [CGSize] = [
	.init(width: 100, height: 100),
	.init(width: 80, height: 120),
	.init(width: 100, height: 100),
	.init(width: 200, height: 200),
	.init(width: 80, height: 100),
	.init(width: 100, height: 120),
	.init(width: 100, height: 80)
]

let normalizedSizes: [CGSize] = sizes.lay_calculate(for: view.bounds.size.width, preferredHeight: 180)

```

## Requirements

- Xcode 8.0+
- iOS 8.0+
- Swift 3.0+

## Installation

### Carthage

For [Carthage](https://github.com/Carthage/Carthage), add the following to your `Cartfile`:

```ogdl
github "min/Lay" ~> 0.1.0
```
