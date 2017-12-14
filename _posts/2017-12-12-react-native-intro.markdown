---
title: Introduction to React Native
date: '2017-12-12 17:00:00'
categories: []
layout: post
author: Kara Waldemer
description: What is React Native and how does it affect a developers day.
slug: react-native-intro
tags: [mobile, react native, react, ios, android, mobile app]
draft: false
---

React Native is a cross-platform solution to writing native mobile applications. Facebook open sourced React Native in March 2015. Facebook built it because, like many companies, they needed to make their product available in the web as well as on various mobile platforms and it was a struggle to maintain the specialized teams needed build the different deployables. After trying a number of different techniques, React Native was Facebook's solution to the problem.


#### What makes React Native Different

There are already solutions to create apps for mobile devices, from writing native code in proprietary languages to writing "mobile web apps" or hybrid solutions. So why do developers need another? Why should they give React Native the time of day?

Unlike other options available React Native allows developers to write native applications on both iOS and Android using JavaScript and a single codebase. It takes the same design principles used by React in the web and lets you write mobile UIs using the familiar component model. In addition, unlike other options that let you use web technologies to create hybrid applications, React Native runs on the device using the same fundamental building blocks used by the platform specific solutions making it a more seamless experience for users. 

<!-- Notes:
React Native lets you build mobile apps using only JavaScript. It uses the same design as React, letting you compose a rich mobile UI from declarative components.

With React Native, you don't build a "mobile web app", an "HTML5 app", or a "hybrid app". You build a real mobile app that's indistinguishable from an app built using Objective-C or Java. React Native uses the same fundamental UI building blocks as regular iOS and Android apps. You just put those building blocks together using JavaScript and React.

React Native lets you build your app faster. Instead of recompiling, you can reload your app instantly. With Hot Reloading, you can even run new code while retaining your application state. Give it a try - it's a magical experience.

React Native combines smoothly with components written in Objective-C, Java, or Swift. It's simple to drop down to native code if you need to optimize a few aspects of your application. It's also easy to build part of your app in React Native, and part of your app using native code directly - that's how the Facebook app works. -->


#### What it does well

React Native has done a lot of maturing over the last few years and offers a lot of benefits when writing mobile applications


##### One Codebase

No need to make changes in multiple places to make sure each platform has all features

<img src="../assets/images/reactNativeIntro/reactNativeiOS1.gif" alt="iOS Inputs" height="500">
<img src="../assets/images/reactNativeIntro/reactNativeAndroid1.gif" alt="iOS Inputs" height="500">

Notes:
Single codebase for both mobile environments with the majority of the code shared.
Helps avoid cases of one platform getting features before another if the other gets it at all.


##### Integration with native components

It is entirely possible to utilize iOS and Android native components and code

<img src="../assets/images/reactNativeIntro/reactNativeiOS2.gif" alt="iOS Inputs" height="500">
<img src="../assets/images/reactNativeIntro/reactNativeAndroid2.gif" alt="iOS Inputs" height="500">

Notes:
Particularly helpful if there is an existing component you want to use on one of the platforms. React Native can just call it and write a separate file for the other platform using one of its native components or a React Native one.


##### Hot Reloading

One of the biggest frustrations of mobile development is constant recompiling

React Native fixes that issue

<img src="../assets/images/reactNativeIntro/reactNativeiOS3.gif" alt="iOS Inputs" height="500">
<img src="../assets/images/reactNativeIntro/reactNativeAndroid3.gif" alt="iOS Inputs" height="500">

Notes:
Just like you can do when using React to develop in the web, when you make a change, you only need to refresh the simulator/emulator to see the change reflected. However, if you change any of the native configurations or code, you will have to recompile. Since most of your code is written in JavaScript this is usually a much less painful process than purely native solutions.



#### What still needs work

As with most technologies that make developers lives easier, React Native is not without its pitfalls

Notes:
It is both a positive and a negative that you are using JS & React. It feels familiar and the learning curve is smaller but it is easy to write 'web' code to run natively and that does not always provide the best mobile user experiences.


##### Performance

Communication between the API controlling the underlying hardware and the JavaScript on the virtual machine is the crux of the problem

Notes:
Animations in particular require a lot of communication, slowing the application down.
Additionally, Android seems to run slower by default.

The second reason this is tough is that there's some fixed amount of overhead associated with every round trip between the native environment and the JavaScript virtual machine. If we need to cross the thread boundary often, we'll have to incur this overhead over and over again.

Since React components are just pure, side-effect-free functions that return what our views look like at any point in time, we never need to read from our underlying rendered view implementation in order to write to it. In the browser environment, React is non-blocking with respect to the DOM, but the beauty of React is that it is abstract and not tightly coupled to the DOM. React can wrap any imperative view system, like UIKit on iOS, for example.

One of the best parts about this approach is that we can adopt it incrementally, building new products on top of it or converting old products to use it whenever and wherever it makes sense.


##### Maturity

React Native is a fairly young technology. It has seen a lot of growth since then, and there are many libraries to pick from, but they too are not that old

Notes:
The progress made in the last two years has made React Native a good contender when writing a mobile solution but the reliability and availability of some of the functionality mobile developers have come to expect is still questionable at times. You may have to develop your own wrappers on top of native code to achieve the results you want but React Native makes it easy to do that and easy to swap it for a different solution later as needed.


#### Conclusion

React Native has a lot of potential but also a lot of room to grow.
