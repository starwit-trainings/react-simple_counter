# Simple Counter in React

## Start a new Project in React, you need NodeJS and NPM
Node.js is a Javascript runtime environment that processes data very quickly and is easy to scale. NPM is a Package Manager which is available for public use. NPM allows us to easily use code written by others without having to write it ourselves during development.

### We are creating a new React project with NPX.
NPX stands for Node Package Execute. NPX comes with NPM, when NPM is installed above the 5.2.0 version, it gets installed automatically. NPX is an NPM package runner and its role is to execute the package from the registry without even installing that package.
```
npx create-react-app simple-counter
```

### Switch to folder 'simple-counter' and start VS-Code
```
cd simple-counter
code .
```

### Start the application now with npm start (runs on localhost:3000), here we can view our result "on-the-fly".
```
npm start
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

### For a simple test, we can insert the following code in line 8 and view it directly in the browser
The 'p' element defines a paragraph of text. Paragraphs are used to structure a text.
```
import logo from './logo.svg';
import './App.css';

function App() {
  return (
    <div className="App">
      <header className="App-header">
        <p>Hello World</p>
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