<div align="center">

<img src="https://raw.githubusercontent.com/jeffreylanters/unity-request-review/master/.github/WIKI/repository-readme-splash.png" width="100%">

</br>
</br>

[![openupm](https://img.shields.io/npm/v/nl.elraccoone.request-review?label=UPM&registry_uri=https://package.openupm.com&style=for-the-badge&color=232c37)](https://openupm.com/packages/nl.elraccoone.request-review/)
[![](https://img.shields.io/github/stars/jeffreylanters/unity-request-review.svg?style=for-the-badge)]()
[![](https://img.shields.io/badge/build-passing-brightgreen.svg?style=for-the-badge)]()

Provides a basic implementation for requesting app reviews for mobile apps on the Apple AppStore and Google PlayStore.

**&Lt;**
[**Installation**](#installation) &middot;
[**Documentation**](#documentation) &middot;
[**License**](./LICENSE.md)
**&Gt;**

</br></br>

[![npm](https://img.shields.io/badge/fund_this_project-sponsor-E12C9A.svg?style=for-the-badge)](https://github.com/sponsors/jeffreylanters)

Hi! My name is Jeffrey Lanters, thanks for checking out my modules! I've been a Unity developer for years when in 2020 I decided to start sharing my modules by open-sourcing them. So feel free to look around. If you're using this module for production, please consider donating to support the project. When using any of the packages, please make sure to **Star** this repository and give credit to **Jeffrey Lanters** somewhere in your app or game. Also keep in mind **it it prohibited to sublicense and/or sell copies of the Software in stores such as the Unity Asset Store!** Thanks for your time.

**&Lt;**
**Made with &hearts; by Jeffrey Lanters**
**&Gt;**

</br>

</div>

# Installation

### Using the Unity Package Manager

Install the latest stable release using the Unity Package Manager by adding the following line to your `manifest.json` file located within your project's Packages directory, or by adding the Git URL to the Package Manager Window inside of Unity.

```json
"nl.elraccoone.request-review": "git+https://github.com/jeffreylanters/unity-request-review"
```

### Using OpenUPM

The module is availble on the OpenUPM package registry, you can install the latest stable release using the OpenUPM Package manager's Command Line Tool using the following command.

```sh
openupm add nl.elraccoone.request-review
```

# Documentation

This module focusses on only requesting a review while trying to keep the code as minimalisic as posible wihout prefabs and monobehaviours.

## Usage

Use the RequestReview namespace, and call the Open method in order to open the review request.

```cs
using ElRaccoone.RequestReview;
public class Main {
  private void Start () {
    RequestReview.Open ();
  }
}
```

## iOS 10.3 or newer notes

The module tells StoreKit to ask the user to rate or review your app, if appropriate.

Although you should call this method when it makes sense in the user experience flow of your app, the actual display of a rating/review request view is governed by App Store policy. Because this method may or may not present an alert, it's not appropriate to call it in response to a button tap or other user action.

When you call this method while your app is still in development mode, a rating/review request view is always displayed so that you can test the user interface and experience. However, this method has no effect when you call it in an app that you distribute using TestFlight.

## iOS 10.2 or lower notes

**Coming soon!**

Support for this platform has yet to be implemented.

## Android notes

**Coming soon!**

Support for this platform has yet to be implemented.
