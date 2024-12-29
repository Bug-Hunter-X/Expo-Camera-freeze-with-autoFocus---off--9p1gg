# Expo Camera Freeze with autoFocus: 'off'

This repository demonstrates a bug in the Expo Camera API where setting `autoFocus` to `'off'` prevents `takePictureAsync` from working correctly. The camera preview freezes, and no picture is taken.  The console does not provide any error messages.

## Bug Reproduction

1. Clone this repository.
2. Run `npm install`.
3. Run `expo start`.
4. Observe the behavior of the camera when you tap the "Take Picture" button (with `autoFocus` set to `'off'`).

## Solution

The solution involves handling the camera's state more explicitly and potentially using a timeout mechanism to trigger the picture-taking process after a slight delay.  The exact approach might depend on your application's requirements and the underlying reasons for the freeze, which appear to be related to asynchronous operations and state management within the Expo Camera API.