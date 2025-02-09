# Inconsistent Deep Linking Behavior with Expo Linking API

This repository demonstrates a bug related to inconsistent deep linking behavior using the Expo `Linking` API. The issue revolves around the `Linking.addEventListener` not firing consistently and `Linking.getInitialURL` sometimes returning `null`. This leads to unpredictable app behavior when attempting to handle deep links.

## Bug Description

The `Linking.addEventListener` for URL changes often fails to trigger, and `Linking.getInitialURL` frequently returns `null`, even when a deep link is present. This prevents the application from properly handling the incoming deep link, leading to unexpected behavior and a poor user experience.

## Solution

The solution involves carefully managing the event listeners, ensuring they're properly attached and detached, and incorporating robust error handling to deal with cases where `Linking.getInitialURL` returns `null`.  This is demonstrated in `bugSolution.js`.

## Reproduction Steps

1. Clone this repository.
2. Run `npm install`.
3. Run the app in Expo Go or on a simulator.
4. Attempt to open a deep link to the app.
5. Observe the inconsistent behavior, sometimes the deep link is handled correctly and other times not.

## Technologies Used

* Expo
* React Native
* JavaScript