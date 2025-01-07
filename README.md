# Firebase Offline Persistence Bug with Deeply Nested Objects

This repository demonstrates a bug encountered with Firebase offline persistence when dealing with deeply nested objects in a React Native application using `@react-native-firebase/firestore`.  The issue manifests as data being written seemingly correctly but not being available offline. The problem is isolated to the nested structure of the data.

## Bug Description

Data is successfully written to Firestore, and `onSnapshot` confirms the write.  However, when offline, retrieving data containing deeply nested objects results in those nested objects being missing or incorrect.  Shallowly structured documents persist correctly.