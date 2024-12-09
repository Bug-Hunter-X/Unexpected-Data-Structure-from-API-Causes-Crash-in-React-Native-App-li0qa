# React Native App Crash Due to Unexpected Data Structure

This repository demonstrates a common bug in React Native applications where the app crashes due to an unexpected data structure received from an API. The app successfully fetches data but crashes when trying to access a property that may not exist in the response.

## Bug Description
The `MyComponent` fetches data from a remote API. If the API response is malformed or doesn't contain the expected properties, the app crashes when trying to access `data.name`.  This is because the component doesn't handle the case where the `data` object might be null, undefined, or lack the `name` property.

## Solution
The solution involves adding proper error handling and null checks to gracefully handle unexpected data structures.

## How to Reproduce
1. Clone this repository.
2. Run `npm install`.
3. Run `npx react-native run-android` or `npx react-native run-ios`.
4. Observe the app's behavior.  If the API response is malformed, the app will crash.
