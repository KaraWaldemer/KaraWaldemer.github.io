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



#### What it does well

There are a number of benefits to developing with React Native over other mobile solutions.



##### One Codebase

One of the nicest features of React Native is that you can write a mobile app that runs natively on both iOS and Android using a single codebase and largely in a single language. Developers can write a single React component using the building blocks provided by React Native and they will run on  different devices using their platforms unique components behind the scenes. The React code that developers build runs on an embedded instance of JavaScriptCore on the device. From there React Native is able to make calls to the native APIs to create the native version of the component. This allows developers to write code once and have it run using the native components and styling on both platforms.

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
