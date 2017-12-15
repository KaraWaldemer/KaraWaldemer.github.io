---
title: Introduction to React Native
date: '2017-12-14 01:00:00'
categories: []
layout: post
author: Kara Waldemer
description: What is React Native and how does it affect a developers day.
slug: react-native-intro
tags: [mobile, react native, react, ios, android, mobile app]
draft: false
image: '../assets/reactNativeIntro/IntroToReactNative.png'
---

React Native is a cross-platform solution to writing native mobile applications. Facebook open sourced React Native in March 2015. They built it because, like many companies, Facebook needed to make their product available in the web as well as on various mobile platforms and it was a struggle to maintain the specialized teams needed to build the different deployables. After trying a number of different techniques, React Native was Facebook's solution to the problem.



#### What makes React Native Different

There are already solutions to create apps for mobile devices: from writing native code in proprietary languages to writing "mobile web apps" or hybrid solutions. So why do developers need another? Why should they give React Native the time of day?

Unlike other options available React Native allows developers to write native applications on both iOS and Android using JavaScript with React in a single codebase. It takes the same design principles used by React in the web and lets you write mobile UIs using the familiar component model. In addition, unlike other options that let you use web technologies to create hybrid applications, React Native runs on the device using the same fundamental building blocks used by the platform specific solutions making it a more seamless experience for users.



#### What it does well

There are a number of benefits to developing with React Native over other mobile solutions:



##### One Codebase

One of the nicest features of React Native is that you can write a mobile app that runs natively on both iOS and Android using a single codebase and, largely, in a single language. Developers can write a single React component using the building blocks provided by React Native and they will run on  different devices using their platforms unique components behind the scenes. The React code that developers build runs on an embedded instance of JavaScriptCore on the device. From there, React Native is able to make calls to the native APIs to create the native version of the component. React Native allows developers to write code once and have it run using native components and styling on both platforms.

###### Native Components

<img src="../assets/images/reactNativeIntro/reactNativeiOS1.gif" alt="iOS Inputs" height="500">
<img src="../assets/images/reactNativeIntro/reactNativeAndroid1.gif" alt="iOS Inputs" height="500">


There are cases, however, where you might not want to rely on the native styling and you want a more unified look across platforms. In that case, React Native allows you to write style sheets where you can overwrite the defaults.



##### Integration with native components

There are instances where, for one reason or another, a developer will need to make use of native components when writing mobile apps. Whether you want to reuse an existing library written in a proprietary language or React Native simply does not provide a solution that works for your use case, you are likely going to run into a case where native code is required. Developers at Facebook had that issue as well and built a solution to it into React Native.

React Native allows developers to create JavaScript wrappers which act as bridges to make native libraries and code available for use in the JavaScript code.

###### Native hardware

<img src="../assets/images/reactNativeIntro/reactNativeiOS2.gif" alt="iOS Inputs" height="500">
<img src="../assets/images/reactNativeIntro/reactNativeAndroid2.gif" alt="iOS Inputs" height="500">


This is a really helpful tool to make available to developers. A thing to remember is that this works on a platform by platform basis. You would have to develop native functionality for each platform in order to make this work properly.


##### Hot Reloading

If you have ever done mobile development, one of the biggest frustrations you have probably faced is constant recompiling. Whenever you make a change to any code or change where a UI element is located, you have to wait for the project to completely recompile before you can check your changes.

React Native fixes this issue. It takes the ability to hot reload that all web developers are familiar with and makes it available on the mobile simulators and emulators. So now with the click of a few keys, developers are able to view their changes as they make them.

###### Hot reload

<img src="../assets/images/reactNativeIntro/reactNativeiOS3.gif" alt="iOS Inputs" height="500">
<img src="../assets/images/reactNativeIntro/reactNativeAndroid3.gif" alt="iOS Inputs" height="500">

An important thing to keep in mind though is that if you change any of the native configurations or code, you will have to recompile. Since most of your code can be written in JavaScript this is usually a much less painful process than when writing a purely native solution.



#### What still needs work

As with most technologies that make developers lives easier, React Native is not without its pitfalls.



##### Performance

The biggest complaint I have seen from developers about React Native is that there can be some real performance issues when developing with it. Facebook has made a lot of progress in improving the performance but it is still something to keep in mind when exploring options.

The crux of the issue boils down to the communication between the APIs controlling the underlying hardware and the JavaScript running on JavaScriptCore. This comes with some overhead because it needs to cross the thread boundary. The more times you have to make that journey, the more overhead is incurred.

Since it is built using React, changes can be made in the virtual DOM and only sent to the native API for rendering when all changes are complete. The problem of over communication is largely mitigated through this model. However, there are still cases where more frequent calls become necessary. In particular, animations are a costly action as they requires constant back and forth communication to make the incremental changes needed in the view. Facebook has recently released a major update to how React Native handles animations which makes this process much less painful. However, it is still important to note that you will likely see performance issues in apps that use a lot of animation.


##### Maturity

As we have seen, React Native is a fairly young technology and while it has seen a lot of growth since its initial release, its "youth" can still cause developers grief. The components provided by Facebook are fairly good and they utilize the underlying native building blocks well. There are still fewer options available than many developers would like. I have found many third party libraries that have tried to fill in some of these gaps, and some of them are really well done, but others could use a lot of work. With its relative youth in mind, it is important to note that you will quite likely need to fall back on writing some native code to achieve the full functionality you want.



##### Usability

I have found that it is both a positive and a negative that React Native allows developers to write mobile apps in JavaScript with familiar React concepts. On the one hand, as a web developer, the learning curve for me to get in to it and get started was a lot smaller than if I had to learn both iOS and Android development separately. On the other hand, I found that it was really easy to fall back into old habits and write "web" code to run natively. What looks good and provides the best experience in the web does not always transfer to a mobile experience. I have to remind myself of this when I am creating and styling my components. It is also important to thoroughly review any third party libraries you plan to use to make sure the user experience is appropriate.


#### Conclusion

Overall, I have been really excited by my experiences working with React Native. It has come a long way since its first release over two years ago and it certainly has a lot of room to grow. React Native has made the jump from web to mobile development much less painful than it could have been and I am looking forward to following it further.

For a glimpse into what React Native code looks like, using Redux, head over to my [GitHub](https://github.com/KaraWaldemer) and check out my [demo project](https://github.com/KaraWaldemer/reactNativeDemo).
