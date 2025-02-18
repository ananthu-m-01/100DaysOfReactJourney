# Day 1: Working with Components Props and JSX

## Topic: React Strict Mode

### What is React Strict Mode?
React Strict Mode is a development tool in React that helps identify potential problems in an application. It does not impact the production build but enables additional checks and warnings during development to ensure best practices are followed.

### Benefits of Using Strict Mode:
- Identifies unsafe lifecycle methods
- Warns about deprecated APIs
- Detects side effects in render phase
- Helps with detecting unexpected behavior in components

### How to Enable Strict Mode:
You can wrap your application in `<React.StrictMode>` in `index.js` or `main.jsx`:

```jsx
import React from "react";
import ReactDOM from "react-dom/client";
import App from "./App";

const root = ReactDOM.createRoot(document.getElementById("root"));
root.render(
  <React.StrictMode>
    <App />
  </React.StrictMode>
);
```

### Key Takeaways:
- **Strict Mode only runs in development** and does not affect production.
- **It helps detect potential issues early** and improves code quality.
- **It encourages better coding practices** by highlighting deprecated features.

## Topic :  Components as Building Blocks

### What is Components
React components are independent, reusable building blocks in a React application that define what gets displayed on the UI. They accept inputs called props and return React elements describing the UI.4

- React applications are entirely made out of Components
- Building blocks of user interfaces in React
- Piece of UI that has its own data, logic and appearances
- We build complex UIs by building multiple components and combaining them
- Components can be reused, nested inside each other and pass data between them
- Parent components : component that has one or more child component
- Child Component : The child components are nested within the parent component

### Rules for creating a React Component
- Component name must start with an uppercase letter React treats lowercase tags as built-in HTML elements (e.g., `<div>`, `<p>`).
- Must return JSX (markup) Components should return valid JSX inside a `return` statement.
- Can be a function or a class (preferably function components) Functional components are the modern standard.
- Must be exported for use in other files 
- Use `export default ComponentName`; or export `{ ComponentName }`;
- Must be wrapped inside a single parent element. Return only one root element (use `<></>` or `<div>` if needed).

### My Learning Experience 📖
Today, I explored how React Strict Mode helps in debugging and enforcing best practices. Implementing it in my project provided insights into how it catches potential issues that might be overlooked.

---
