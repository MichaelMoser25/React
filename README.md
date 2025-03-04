# React
- React is a JavaScript library for building user interfaces
- React is used to build single-page applications
- React allows us to create reusable UI components

```
import React from 'react'
import ReactDOM from 'react-dom/client';

funtction Hello(props) {
  return <h1>Hello World!</h1>;
}

const container = document.getElementById("root");
const root = ReactDOM.createRoot(container);
root.render(<Hello />);
```

Command to run React application: ```npx create-react-app my-team```
