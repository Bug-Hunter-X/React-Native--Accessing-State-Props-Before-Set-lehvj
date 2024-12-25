# React Native: Accessing State/Props Before Set

This repository demonstrates a common yet subtle error in React Native: attempting to access state or props before they have been fully initialized.  This often occurs with asynchronous operations.

The `bug.js` file shows the problematic code, while `bugSolution.js` presents a solution using asynchronous operations and conditional rendering to handle the data loading process gracefully.

## Steps to Reproduce

1. Clone the repository.
2. Navigate to the repository's directory.
3. Run `npm install` to install dependencies.
4. Run `npx react-native run-android` (or `npx react-native run-ios`) to run the app on your emulator/device.
5. Observe the error in the console (if not properly handled) and the corrected behaviour in `bugSolution.js`

## Solutions

* **Conditional Rendering:** Only render the component that depends on the state or prop after it has been set.  Check if your data is loaded before trying to use it.
* **Asynchronous Operations:** Correctly handle asynchronous operations using `.then()` for promises or `async/await` for improved readability and easier error handling.