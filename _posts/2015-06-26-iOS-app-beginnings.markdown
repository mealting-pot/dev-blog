---
title:  "iOS app beginnings"
date:   2015-06-26 20:00:00
description: iOS App creation
---

Hello,

So yesterday I have put some work on the iOS app. I also want to use this project as a way to practice the Swift (2.0) language and learn the new iOS API as much as I can.

So here is a list of what I did already :
  
* I enhanced the skeletton logic I had created before and now it choose between storyboards at runtime to route the user to either the login storyboard or the main storyboard.  
   In time, it will use the new Xcode 7 storyboard reference feature.

* I also struggled 3 hours with an Xcode 7 bug when I tried to update my pods...  
   If your app is crashing on startup only on device because of a missing pods framework (only if you use the `use_frameworks!` flag because you use a swift pod such as Alamofire), try to disable the new bitcode feature (`ENABLE_BITCODE = NO` in the .plist).  
   The cause is a conflict betweens pods (`weak_frameworks`) and bitcode at the moment.  

* Then I started designing the MealsViewController, the view controller that will display all the available meals around your location.  
   I wanted a modular design for the cells with differents features depending of the device orientation (like a map for when the cells are displayed on iPad), so I maximized my use of the new `UIStackView` (which are awesome btw, even if there is still some issues I do not know properly how to fix... the same feeling as using scrolls views with Autolayout when you don't know the littles trics :) ).  
   After hours of fighting, I finished with a design for the cell, which is 100% Autolayout "responsive", that I'm proud of. (Next time I will put screenshot ;) )
  
  
And that's all for this time,  
Valentin Pertuisot  
