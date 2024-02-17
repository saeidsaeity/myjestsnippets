# Snippet Extension README

## Description
This Visual Studio Code extension provides several useful code snippets to enhance your development workflow. It includes snippets for common testing scenarios in JavaScript.

## Installation
To install this extension, follow these steps:

1. Open Visual Studio Code.
2. Go to the Extensions view by clicking on the square icon in the sidebar or pressing `Ctrl+Shift+X`.
3. Search for "Snippet Extension" in the Extensions Marketplace.
4. Click on the Install button.

## Usage
Once installed, you can use the snippets by typing their trigger keywords in a JavaScript file and pressing `Tab` to insert the snippet.

### Available Snippets

#### `mut`
This snippet provides test cases for testing mutable functions. It includes two test cases:
- Test whether the function returns a different reference to the input array.
- Test whether the function does not mutate the input array.

#### `comp`
This snippet provides a test case for testing the return value of a function.

#### `typetest`
This snippet provides a test case for testing the return type of a function.

## Example
```javascript
// Type `mut` and press `Tab` to insert the snippet
test('should be different reference to input', () => {
  const input = [];
  expect(func(input)).not.toBe(input);
});

test('should not mutate input', () => {
  const input = [];
  const copyinput = [];
  func(input);
  expect(input).toEqual(copyinput);
});