 # Pluto Swift Client SDK

![CI Status](https://github.com/MuShare/PlutoSwiftClientSDK/workflows/build_check/badge.svg?branch=master)
[![Version](https://img.shields.io/cocoapods/v/PlutoSDK.svg?style=flat)](https://cocoapods.org/pods/PlutoSDK)
[![License](https://img.shields.io/cocoapods/l/PlutoSDK.svg?style=flat)](https://cocoapods.org/pods/PlutoSDK)
[![Platform](https://img.shields.io/cocoapods/p/PlutoSDK.svg?style=flat)](https://cocoapods.org/pods/PlutoSDK)

Swift SDK for Pluto login microservice, which simplify the implementation for signing in with email, Google and Apple.

## Installation

The Swift SDK for Pluto is available through [CocoaPods](https://cocoapods.org). To install
it, simply add the following line to your Podfile:

```ruby
pod 'PlutoSDK'
```

## Document

To auth with Pluto, set up it at first in your `AppDelegate` class.

```swift
Pluto.shared.setup(server: "[server url]", appId: "[app id]")
```

### Sign in, Sign up and Sign out

Implement signing in and signing up with the following methods

- `Pluto.shared.register()`
- `Pluto.shared.resendValidationEmail()`
- `Pluto.shared.loginWithAccount()`
- `Pluto.shared.loginWithGoogle()`
- `Pluto.shared.loginWithApple()`
- `Pluto.shared.resetPassword()`
- `Pluto.shared.logout()`

### Token Management

After signing in, get token or the header with token with the following methods

- `Pluto.shared.getToken()`
- `Pluto.shared.getHeaders()`

Get and update user information with 

- `Pluto.shared.currentUser`
- `Pluto.shared.myInfo()`
- `Pluto.shared.updateName()`
- `Pluto.shared.uploadAvatar()`

Get scopes from jwt token with

- `Pluto.shared.getScopes()`

### Account Binding

Bind and unbind accounts

- `Pluto.shared.bind()`
- `Pluto.shared.unbind()`

Get avaliable login types and bindings

- `Pluto.shared.availiableLoginTypes`
- `Pluto.shared.availiableBindings`

### Debug

Support the following debug method for `DEBUG` and `ADHOC` mode:
- `Pluto.shared.simulateInvalidRefreshToken`
- `Pluto.shared.simulateInvalidAccessToken`
- `Pluto.shared.resetExpire`

## Author

lm2343635, lm2343635@126.com

## License

 Pluto Swift Client SDK is available under the MIT license. See the LICENSE file for more info.
