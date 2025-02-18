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

### My Learning Experience 📖
Today, I explored how React Strict Mode helps in debugging and enforcing best practices. Implementing it in my project provided insights into how it catches potential issues that might be overlooked.

---
