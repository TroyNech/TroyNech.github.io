---
title: Contact Manager App
---

**[Code](https://github.com/TroyNech/contactor)**

[Skip to the demo video](#demo)

## Description

The project is a mobile app for managing contacts. It is designed for use in group settings like networking events where people want to exchange contact information. The app can display a QR code containing users’ contact information, which other users scan using the app. Scanned QR codes are then decoded to get the contact information, and then the contact is added to the scanning user’s contact list. This app provides superior functionality over other methods in group situations because people are able to exchange contact information with a minimal amount of steps. A person just needs to display their QR code until everyone has scanned it, then press the Scan button to scan the codes of everyone else as they take turns displaying QR codes. There is no need to go through menus and prompts like there is for Wi-Fi Direct and similar methods. It is also cross-platform, unlike Android Beam and NFC.

## Design

The app was built using the Ionic 4 framework. Ionic allows developers to create a single project that can run on multiple platforms, including iOS and Android, using web technologies. Ionic 4 provides a front-end framework that reduces the amount of work developers need to do by having readymade components and styling. The main programming language of Ionic is JavaScript. The Angular JavaScript framework was used as it is recommended for Ionic 4. Angular allows for the creation of single page apps and follows an MVC architecture. It is especially useful because it provides dependency injection, templates, lots of useful library functions and it takes care of modifying the DOM by itself.

Google’s Firebase web and application development service was used to provide critical functionality for the app. Firebase allows developers to create serverless applications by providing server functionality that is accessible through APIs. This app uses Firebase Authentication and Firestore, both of which are free at low levels of usage. Firebase Authentication takes care of the authenticating users. Given an email and a password, it can create an account or tell if it is a valid login. Password reset emails are also sent using Firebase Authentication. Firebase Firestore is a NoSQL database that stores data in a key-value format similar to JSON. One of its crucial features is that it syncs data immediately and will track updates while devices are offline, syncing with the server once the device becomes connected. It also caches data so requests will use local data while the device is offline. Firestore was used to store of the users’ account information.

## Demo

<video height="500" controls>
  <source src="demo.mp4" type="video/mp4">
</video>