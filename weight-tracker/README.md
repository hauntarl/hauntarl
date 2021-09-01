#  Weight Tracker

Record personal weight information periodically in order to share with a third party such as a doctor or friend.

<img src="https://github.com/hauntarl/hauntarl/blob/master/weight-tracker/intro-demo.gif" width="250"> <img src="https://github.com/hauntarl/hauntarl/blob/master/weight-tracker/home-demo.gif" width="250">

## Features:

### Onboarding Slides (one-time setup, also acts as settings menu)

- Store user name
- Store user email
- Select recipient from contacts or create new if needed
- Save weight unit (Pounds/Kilograms)

### Home Page (create new weight entry)

- Weather updates from [openweathermap.org](https://openweathermap.org/)
- Date/Time input using `UIDatePickerView` (default: shows user the current time until user starts interacting) 
- Weight slider (default: last entered)
- Log button (stores data into MongoDB Realm)
- View/Edit History button
- Settings button to update user preferences and information

### History Page (table displaying weight logs)

- Cell Structure:
  - Weight information in user selected unit
  - Time difference from now
  - Deviation from average of all weight logs
- Swipe to see detailed information about each log 
- Swipe to delete feature for cells
- Share weight report for selected/all logs (via email, message or other apps based on user selected recipient information)

## Architecture and Design Patterns

### Model View Presenter [architecture]( https://saad-eloulladi.medium.com/ios-swift-mvp-architecture-pattern-a2b0c2d310a3)

### Behavioural design patterns

- [Chain of responsibility](https://github.com/ochococo/Design-Patterns-In-Swift#-chain-of-responsibility) pattern - `WeatherDataPresenter` used for delegation of tasks
- [Iterator](https://github.com/ochococo/Design-Patterns-In-Swift#-iterator) pattern - `Results<WeightData>` comes with Realm Dependency

### Creational design patterns

- [Singleton](https://github.com/ochococo/Design-Patterns-In-Swift#-singleton) pattern  - `UserDefaults.standard` used to store shared preferences

### Structural design patterns

- [Façade](https://github.com/ochococo/Design-Patterns-In-Swift#-fa%C3%A7ade) pattern - `Models/UserDetails` creates a layer of abstraction on `UserDefaults.shared`

## Packages and Dependencies

### [SwiftyGif](https://github.com/kirualex/SwiftyGif) - High performance & easy to use Gif engine

- UIImage and UIImageView extension based
- Remote GIFs with customizable loader
- Great CPU/Memory performances
- Control playback
- Allow control of display quality by using 'levelOfIntegrity'
- Allow control CPU/memory tradeoff via 'memoryLimit'

### [IQKeyboardManager](https://github.com/hackiftekhar/IQKeyboardManager) - Codeless drop-in universal library allows to prevent issues of keyboard sliding up and cover UITextField/UITextView. 

- **CODELESS**, Zero Lines of Code
- Works Automatically
- No More UIScrollView
- No More Subclasses
- No More Manual Work
- No More #imports

### [realm-cocoa](https://github.com/realm/realm-cocoa) - Realm is a mobile database: a replacement for Core Data & SQLite

- **Intuitive to Developers:** Object-oriented data model is simple to learn, doesn’t need an ORM, and lets you write less code.
- **Designed for Offline Use:** Realm’s local database persists data on-disk, so apps work as well offline as they do online.
- **Built for Mobile:** Realm is fully-featured, lightweight, and efficiently uses memory, disk space, and battery life.

### [SwipeCellKit](https://github.com/SwipeCellKit/SwipeCellKit) - Swipeable `UITableViewCell`/`UICollectionViewCell`

- Left and right swipe actions
- Action buttons with: text only, text + image, image only
- Customizable transitions: Border, Drag, and Reveal
- Customizable action button behavior during swipe
- Animated expansion when dragging past threshold
- Customizable expansion animations
- Support for both UITableView and UICollectionView

## Asset Catalogue

### App Icon

- [Diet concept drawing weight legs hotdog](https://all-free-download.com/free-vector/download/diet-concept-drawing-weight-legs-hotdog-icons_6834721.html#google_vignette) is free to use as long as app isn't used commercially
- [App Icon Generator](https://appicon.co/)

### Color Palette - [Colorhunt](https://colorhunt.co/palettes/popular)

- Background Color: `#F0F5F9`
- Primary Color: `#1E2022`
- Secondary Color: `#52616B`
- Tint Color: `#C9D6DF`
- Accent Color: `#FC5185`

#### Misc

- Hightlight Color: `#3F3C56`
- Positive Color: `#50CB93`
- Negative Color: `#F8485E`

### Illustrations and GIFs

- Welcome GIF by **[jp loridan @LottieFiles](https://lottiefiles.com/9517-welcom)** with [Creative Commons License 4.0](https://lottiefiles.com/page/license)
- Illustrations from [Undraw.co](https://undraw.co/illustrations) with [license](https://undraw.co/license) for free commercial use

### Fonts

- [Pacifico](https://fonts.google.com/specimen/Pacifico) Google Fonts with [license](https://fonts.google.com/specimen/Pacifico#license) for free commercial use
- [Quicksand](https://fonts.google.com/specimen/Quicksand) Google Fonts with [license](https://fonts.google.com/specimen/Quicksand#license) for free commercial use

