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

### Create React App
- To learn and test React, you should set up a React Environment on your computer.
- This tutorial uses the create-react-app.
- The create-react-app tool is an officially supported way to create React applications.
- Node.js is required to use create-react-app.
- Open your terminal in the directory you would like to create your application.
- Run this command to create a React application named my-react-app:



Note: If you've previously installed ```create-react-app``` globally, it is recommended that you uninstall the package to ensure npx always uses the latest version of ```create-react-app```. To uninstall, run this command: ```npm uninstall -g create-react-app```.

### Run the React Application
Run this command to move to the ```my-react-app``` directory:
```cd my-react-app```

Run this command to execute the React application ```my-react-app```:
```npm start```

A new browser window will pop up with your newly created React App! If not, open your browser and type localhost:3000 in the address bar.

### How Does React Work?
- React creats a VIRTUAL COM in memory
    - Instead of manipulating the browser's DOM directly, React creates a virtual DOM in memory, where it does all the necessary manipulating, before making the changes in the browser DOM.
























