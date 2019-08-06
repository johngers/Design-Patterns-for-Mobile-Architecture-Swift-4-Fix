# Design-Patterns-for-Mobile-Architecture-Swift-4-Fix
This is a guide on how to get the Exercise files for the iOS App Development Course 
"Design Patterns for Mobile Architecture" to Swift 4.

First you have to go into the excerise files and go to the folder "03_01__start" as this
is the point in the course where you start to code. 

Then open the remove everything except the "KnownSpys" folder and the "KnownSpys.xcodeproj".

Now open the Xcode project for the excercise. Click on "KnownSpys" in the Project Navigator. 

Then, click on "KnownSpys" in the Targets. Go to Build Settings and search for "Swift Language Version". 
Change this to Swift 4.0

Next, you want to reinstall the CocoaPods.

Assuming you already have CocoaPods installed, travel to project directory with your Terminal and type:

**pod init**

Then type:

**open -a Xcode Podfile**

Paste this as your Podfile: 
____________________________________________________________________________________________

# Uncomment the next line to define a global platform for your project
# platform :ios, '10.0'

target 'KnownSpys' do
  # Comment the next line if you're not using Swift and don't want to use dynamic frameworks
  use_frameworks!

  # Pods for KnownSpys
    pod 'Swifter'
    pod 'Alamofire'
    pod 'Swinject'
    pod 'RxSwift'
    pod 'RxCocoa'
    pod 'RxDataSources'
    pod 'Outlaw', :git => 'https://github.com/Molbie/Outlaw.git'
    pod 'Toaster'
    pod 'SwinjectStoryboard', :git=> 'https://github.com/Swinject/SwinjectStoryboard.git'
end

____________________________________________________________________________________________

By removing the version numbers we can get the latest versions of all the CocoaPods which have been converted to Swift 4 already.

Now just open the workspace and you should be able to fix the few errors that come up when building the project. After which you can migrate to Swift 5 if you would like.

**I'm not going to upload the fixed files because the rights of the course and source code are not mine**
