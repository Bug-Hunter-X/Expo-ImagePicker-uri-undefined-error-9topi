# Expo ImagePicker 'uri' undefined error

This repository demonstrates a common error when using the Expo ImagePicker library: accessing the `uri` property of a selected image before it's fully loaded.  The example shows how this can lead to an error and how to resolve it.

## Problem

The `launchImageLibraryAsync` or `launchCameraAsync` functions in Expo's ImagePicker library return a promise.  If you attempt to access the image's `uri` immediately after calling these functions, it might be undefined, resulting in an error. 

## Solution

The solution is to use `.then()` to handle the promise and access the `uri` only after the image has been successfully loaded. This ensures that the `uri` is available before your code attempts to use it.
