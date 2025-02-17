# React Native Dimensions API Orientation Bug

This repository demonstrates a common bug in React Native where the `Dimensions` API fails to update its values when the screen orientation changes. This can lead to layout problems where components are not positioned correctly after rotating the device.

## Bug Description
The issue is that the `Dimensions` API doesn't trigger updates on orientation changes. This means any component relying on `Dimensions.get('window').width` or `Dimensions.get('window').height` will retain the old values, resulting in incorrect layouts.

## Solution
The solution involves using the `Dimensions.addEventListener` to listen for orientation changes and update the state accordingly. This ensures that the component re-renders with the correct dimensions.