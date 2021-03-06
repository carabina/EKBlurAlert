# EK Blur Alert


Create an EK Blur Alert View for light actions in iOS Apps.

EK Blur Alert View is a framework created to recreate Apple's private Modal Status View.
While designing iOS apps we may want to alert the user to a successful completion of a task.
When we create applications we need help for users about the completion of certain operations.
This framework will help you to make the same hints as in applications from Apple's music app or podcast app.

Apple's solution is to display a self-removing and small modal view to the screen.

![text](https://raw.githubusercontent.com/emvakar/EKBlurAlert/master/music%20app%20template.png "Apple's custom use of Modal Status Views")

With uses in the News app, the Apple Music app, and the Podcasts app, developers have been wanting access to this view for a while now.
That is what this framework solves.

## Install

### Cocoapods
```ruby
source 'https://github.com/emvakar/EKBlurAlert.git'

pod 'EKBlurAlert'
```
### Manualy

Simply import the framework and add the following code to get started.


### How to use

```swift
import EKBlurAlert

let alertView = EKBlurAlertView(frame: self.view.bounds)
view.addSubview(alertView)
```

Further customize the EKBlurAlertView with the following functions:

```swift
import EKBlurAlert

func presentBluredAlertView() {
    let alertView = EKBlurAlertView(frame: self.view.bounds)
    let myImage = UIImage(named: "yourImageName") ?? UIImage()
    alertView.setCornerRadius(10)
    alertView.set(autoFade: true, after: 7)
    alertView.set(image: myImage)
    alertView.set(headline: "Head Title text")
    alertView.set(subheading: "subtitle text")
    view.addSubview(modalView)
}
```
## Features

### Animations

The EKBlurAlertView will appear and disappear with a fast fading and scaling effect to match Apple's implementation.

### Timer

The EKBlurAlertView will only appear for a couple seconds so as not to interfere with the UX of your app.

### Style

The EKBlurAlertView is designed to match the style and aesthetics of Apple's implementation.

This includes slightly rounded corners,
a blurred visual effects view as the background,
heading and subheading options in addition to an image,
and placement in the center of the view.
The animations were designed to match Apple's original design.

