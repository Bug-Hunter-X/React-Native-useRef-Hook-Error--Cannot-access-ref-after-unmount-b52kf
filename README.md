# React Native useRef Hook Error: Cannot access ref after unmount

This repository demonstrates a common error in React Native when using the `useRef` hook.  The error occurs when attempting to access the value of a ref after the component containing that ref has unmounted.  The solution involves careful timing and cleanup to prevent accessing a stale ref.

## Bug Description

The bug occurs in `bug.js`.  The code uses `useRef` to hold a reference to a Text component.  However, the ref might be accessed after the component is unmounted which causes the error.  This is a timing issue.

## Solution

The solution (`bugSolution.js`) focuses on preventing the erroneous access.  While it is not always possible to directly prevent this based on timing, making sure cleanup is done properly and any references are explicitly set to null can prevent this type of error.