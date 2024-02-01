# Simple Counter in React

## Start a new Project in React, you need NodeJS, NPM and Vite
Node.js is a Javascript runtime environment that processes data very quickly and is easy to scale. NPM is a Package Manager which is available for public use (see https://www.npmjs.com/). Dependencies resolved via npm are listed in the package.json. The command `npm install` creates a folder `node-modules` in your project directory and downloads all dependencies. Vite is a build tool that aims to provide a faster and leaner development experience for modern web projects.

### First install NodsJS and Vite.
NodeJS can be found on https://nodejs.org/en/download. Download the Build you need and install it, then install Vite.
```bash
npm install -d create-vite
```

### We are creating a new React project with Vite.
```
npm create vite@latest
```
Now you have to choose the Name for the Project (choose simple-counter), the Framework (choose React) and Javascript as Variant

### Switch to folder 'simple-counter', install Node Packages.
```
cd simple-counter
npm install
```

### Start the application now with npm start (runs on localhost:3000 in your Browser), here we can view our result "on-the-fly", then start VSCode
```
npm start
code .
```

### In the directory tree of VS-Code we change to src/App.js and delete all commands that we do not need for our project, the result should look like this
```
import logo from './logo.svg';
import './App.css';

function App() {
  return (
    <div className="App">
      <header className="App-header">
    
      </header>
    </div>
  );
}

export default App;
```

## Write a Programm in React

### We set an initial value of 0 via the useState function and show the output on the Screen
useState returns an array that is split into two constants: while the first value is the representation of the current state, the second value is a function with which this state can be manipulated.
```
import logo from './logo.svg';
import './App.css';
import { useState } from 'react';
function App() {

  const [value, setValue] = useState(0);

  return (
    <div className="App">
      <header className="App-header">
        <p>Value: <span>{value}</span></p>        
      </header>
    </div>
  );
}

export default App;
```

### Add 2 buttons that count up or down the value on click
Whenever you need to perform an action after clicking a button, link, or pretty much any element, you’ll use the onClick event handler.
```
import logo from './logo.svg';
import './App.css';
import { useState } from 'react';
function App() {

  const [value, setValue] = useState(0);

  return (
    <div className="App">
      <header className="App-header">
        <p>Value: <span>{value}</span></p>
        <div>
          <button onClick={() => setValue(value + 1)}>+</button>
          <button onClick={() => setValue(value - 1)}>-</button>
          </div>       
      </header>
    </div>
  );
}

export default App;
```

The result can be viewed in a browser