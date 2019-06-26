## Example project for React Native Issue 18899
As requested by @gaearon [here](https://github.com/facebook/react-native/issues/18899#issuecomment-504218594) to replicate [React Native Issue #18899](https://github.com/facebook/react-native/issues/18899)

## Replication Steps

With `App` component defined as a class, Hot Reload works fine.

To reproduce the issue, comment out the following lines:

https://github.com/chuttam/react-native-hotreload-issue18899/blob/master/App.js#L19-L29

and uncomment out the following lines:

https://github.com/chuttam/react-native-hotreload-issue18899/blob/master/App.js#L31-L38

App content now no longer refreshes on file saves, even though the "Hot Reloading" toast message still appears on the device.

Note: I have only tested Hot Reload with this Demo app on an Android device. No access to iOS emulator/device.

## Setup Notes
Demo project is essentially the result of generating a new, vanilla React Native project.

```
$ watchman --version
4.9.0

$ node -v
v8.9.3

$ react-native init HotReloadIssue18899

$ cd HotReloadIssue18899

$ react-native -version
react-native-cli: 2.0.1
react-native: 0.59.9

$ react-native run-android
```
