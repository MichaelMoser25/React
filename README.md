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

- React only changes what needs to be changed!
    - React finds out what changes have been made, and changes only what needs to be changed. 

# React Directly in HTML
Start by including three scripts, the first two let us write React code in our JavaScripts, and the third, Babel, allows us to write JSX syntax and ES6 in older browsers.

Include three CDN's in your HTML file:
```
<!DOCTYPE html>
<html>
  <head>
    <script src="https://unpkg.com/react@18/umd/react.development.js" crossorigin></script>
    <script src="https://unpkg.com/react-dom@18/umd/react-dom.development.js" crossorigin></script>
    <script src="https://unpkg.com/@babel/standalone/babel.min.js"></script>
  </head>
  <body>
    <div id="mydiv"></div>

    <script type="text/babel">
      function Hello() {
        return <h1>Hello World!</h1>;
      }

      const container = document.getElementById('mydiv');
      const root = ReactDOM.createRoot(container);
      root.render(<Hello />)
    </script>
  </body>
</html>
```
This way of using React can be OK for testing purposes, but for production you will need to set up a React environment.

## Setting up a React Environment
If you have npx and Node.js installed, you can create a React application by using ```create-react-app```

Run this command to move to the my-react-app directory:
```cd my-react-app```

Run this command to run the React application my-react-app:
```npm start```

A new browser window will pop up with your newly created React App! If not, open your browser and type localhost:3000 in the address bar.

### Modify the React Application
Look in the my-react-app directory, and you will find a src folder. Inside the src folder there is a file called App.js, open it and it will look like this:
```
import logo from './logo.svg';
import './App.css';

function App() {
  return (
    <div className="App">
      <header className="App-header">
        <img src={logo} className="App-logo" alt="logo" />
        <p>
          Edit <code>src/App.js</code> and save to reload.
        </p>
        <a
          className="App-link"
          href="https://reactjs.org"
          target="_blank"
          rel="noopener noreferrer"
        >
          Learn React
        </a>
      </header>
    </div>
  );
}

export default App;
```

Example
- Replace all the content inside the <div className="App"> with a <h1> element.
- See the changes in the browser when you click Save.
```
function App() {
  return (
    <div className="App">
      <h1>Hello World!</h1>
    </div>
  );
}

export default App;
```

Click the "Run Example" button to see the result.
index.js:
```
import React from 'react';
import ReactDOM from 'react-dom/client';

const myFirstElement = <h1>Hello React!</h1>

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(myFirstElement);
```

# Upgrade React
Upgrading an existing React application to version 18 only requires two steps.

### Step 1: Install React 18
To install the latest version, from your project folder run the following from the terminal:
```
npm i react@latest react-dom@latest
```

### Step 2: Use the new root API
In order to take advantage of React 18's concurrent features you'll need to use the new root API for client rendering.
```
// Before
import ReactDOM from 'react-dom';
ReactDOM.render(<App />, document.getElementById('root'));

// After
import ReactDOM from 'react-dom/client';
const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<App />);
```
Your application will work without using the new root API. If you continue to use ReactDOM.render your application will behave like React 17.

# React ES6
- ES6 stands for ECMAScript 6

React uses ES6, and you should be familiar with some of the new features like:
- Classes
- Arrow Functions
- Variables (let, const, var)
- Array Methods like .map()
- Destructuring
- Modules
- Ternary Operator
- Spread Operator

## React ES6 Classes
A class is a type of function, but instead of using the keyword function to initiate it, we use the keyword class, and the properties are assigned inside a constructor() method.
```
class Car {
  constructor(name) {
    this.brand = name;
  }
}
```

Create an object called "mycar" based on the Car class:
```
class Car {
  constructor(name) {
    this.brand = name;
  }
}

const mycar = new Car("Ford")
```
### Method in Classes
Create a method named "present":
```
class Car {
  constructor(name) {
    this.brand = brand;
  }

  present() {
    return 'I have a ' + this.brand;
  }
}

const mycar = new Car("Ford");
mycar.present();
```
As you can see in the example above, you call the method by referring to the object's method name followed by parentheses (parameters would go inside the parentheses).

### Class Inheritance
- To create a class inheritance, use the extends keyword.
- A class created with a class inheritance inherits all the methods from another class:

Create a class named "Model" which will inherit the methods from the "Car" class:
```
class Car{
  constructor(name){
    this.brand = name;
  }
}

class Model extends Car {
  constructor(name, mod) {
    super(name);
    this.model = mod;
  }
  show() {
    return this.present() + ', it is a ' + this.model
  }
}

const mycar = new Model("Ford", "Mustang");
mycar.show();
```
- The ```super()``` method refers to the parent class.
- By calling the ```super()``` method in the constructor method, we call the parent's constructor method and get access to the parent's properties and methods.

## React ES6 Arrow Functions












