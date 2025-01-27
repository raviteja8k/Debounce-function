# Debounce Example: Input Text with Keyup

This repository demonstrates a simple implementation of a debounce function in JavaScript, applied to an input text field to optimize event handling for the `keyup` event.

## What is Debouncing?

Debouncing is a programming technique used to ensure a function is executed only after a specific period of inactivity. This is useful in scenarios where frequent function calls (like typing in a search bar) can lead to performance issues or unnecessary API requests.

In this example, the `handleInputChange` function is debounced with a wait time of 500ms. This ensures the function is called only when the user has stopped typing for at least 500ms.

## Implementation

### Debounce Function
The `debounce` function wraps any callback and ensures it is executed only after the specified delay:
```javascript
function debounce(func, wait) {
  let timeout;

  return function (...args) {
    clearTimeout(timeout); // Clear the previous timeout
    timeout = setTimeout(() => func.apply(this, args), wait); // Set a new timeout
  };
}
```

## Running the Example
1. Copy the code into a .html file.
2. Open the file in a browser.
3. Open the browser console to observe the output when typing in the input field.