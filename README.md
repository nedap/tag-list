# TagsList

[![Swift Package Manager](https://img.shields.io/badge/SPM-supported-brightgreen?style=flat)](https://swift.org/package-manager)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=flat)](https://opensource.org/licenses/MIT)
[![Swift 5.4](https://img.shields.io/badge/swift-5.4-blue.svg?style=flat)](https://developer.apple.com/swift/) 


<p align="center">
<b>TagList</b> allows to add a list of highly customizable tags. You can set common tags parameters, add items with unique parameters
</p>


## Example

To run the example project, clone the repo, and run `pod install` from the Example directory first.
Example project includes 3 parts:
- VC is `TagsListDataSource` + customisation of items
- Simple way to display string array (`DefaultTagsListDataSource`)
- Sample of using `TagsList` inside of `UITableViewCell` and calculating `TagsList` height


## Preview

| **Content orientation** | **Items deleting** | **Customisation features** |
|:-------:|:-------:|:-------:|
|<img src="https://github.com/inomobile/tag-list/blob/master/DemoGif/TagList%201.gif?raw=true" width="300">|<img src="https://github.com/inomobile/tag-list/blob/master/DemoGif/TagList%202.gif?raw=true" width="300">| <img src="https://github.com/inomobile/tag-list/blob/master/DemoGif/TagList%203.gif?raw=true" width="300">|
## Requirements

- iOS 10.0+
- Xcode 9.0


## Installation

TagsList is available through [Swift Package Manager](https://cocoapods.org). To install
it, simply add the following to your `Package.swift:`:

```swift
dependencies: [
.package(url: "https://github.com/nedap/tag-list.git", .exact("0.2.0"))
]
```

Import `TagsList` into your swift source file

``` swift
import TagsList
```

Congratulations!

## Usage

### Common tags settings
First step to customise appearance of tags is configure `TagViewItemConfigurator`. It include common tags view settings and applies by default.
<details><summary> TagViewItemConfigurator properties </summary>
<br>

    borderMarginHorizontal
    spacing
    contentHeight
    cellHeight
    itemCornerRadius
    sideImageCornerRadius
    xButtonCornerRadius

    sideImageEverytimeDisplaying
    xButtonEverytimeDisplaying
    maxWidth
    titleFont

    backgroundColor
    sideImageBackgroundColor
    xButtonBackgroundColor
    textColor

    xButtonImage
</details>

### Ways of data representation

Next step is representation of your data. 
There are 2 ways: 
- Create `DefaultTagsListDataSource` and put your string array into
- Set `TagsList` property `tagsListDataSource` and implement methods of `TagsListDataSource` protocol

Choose first way if you need to represent array of strings quickly.
If you want to create tags with different representation I recomend you to use second way or create own TagsListDataSource

### Tags with different representation

If you need to show custom tags like on [Preview](#preview) use `TagViewItem`s array with second way of data representation.
<details><summary> TagViewItem properties </summary>
<br>

    title
    titleColor
    titleFont

    sideImage
    sideImageBackgroundColor

    xButtonDisplaying
    xButtonBackgroundColor
    xButtonImage

    backgroundColor
</details>

If you stil want to customise items after previous steps use `tagsListCellFinalConfiguration` method of `TagsListDataSource`

## Author

Mobile team of Inostudio.

## License

TagsList is available under the MIT license. See the LICENSE file for more info.
