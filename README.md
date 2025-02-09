# React Native AsyncStorage Data Type Handling Bug

This repository demonstrates a common error when working with AsyncStorage in React Native: improper handling of JSON data retrieved using `AsyncStorage.getItem`.  The bug arises from incorrectly treating the retrieved string as a JSON object without parsing it.

## Bug Description
When you store a JSON object in AsyncStorage and then attempt to access its properties directly after retrieval, you encounter a type error because `AsyncStorage.getItem` returns a Promise resolving to a string representation of your JSON object.

## Solution
The solution involves parsing the retrieved string using `JSON.parse()` before attempting to access its properties.

## How to Reproduce
1. Clone this repository.
2. Run `npm install`.
3. Run the app on a simulator or device.
4. Observe the console error in the problematic code example.
5. Observe the corrected functionality after implementing the fix.