# waitForElements

### A JavaScript library to wait for specific elements to load in the DOM.

#### Introduction

This small library is used to wait for elements until they're found in the DOM using the [MutationObserver](https://developer.mozilla.org/en-US/docs/Web/API/MutationObserver) API.

#### Files

###### Minified

Minified is a ready-to-use version. Denoted by the `.min` in the file name. It's basically the same thing but just no unnecessary characters, to improve the performance. 

You can use it in your userscript or project directly through [Github]().

###### Unminified

Unminified is a version to edit, modify, or just simple clean code. It's the one with no `.min` in the file name.

You can use it in your userscript or project directly through [Github]().

#### Usage

Call the function, then pass the element you're looking for. It's done using the [`document.querySelector()`](https://developer.mozilla.org/en-US/docs/Web/API/Document/querySelector) method.

You're being returned the DOM element reference to do anything with element.

In case of success, the element is found, you can do anything within the `.then()` method.

```javascript
waitForElm(".some-class").then((elm) => {
    console.log("Element is ready!");
});
```

Also, you can use it with an [async function](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/async_function).

```javascript
const elm = await waitForElm('.some-class');
```