# Simple Counter in React

## Start a new Prohect in React
You need NodeJS und NPM

### We are creating a new React project with NPX
```
npx create-react-app simple-counter
```

### Switch to folder 'simple-counter' and start VS-Code
```
cd simple-counter
code .
```

### Start the application now with npm start (runs on localhost:3000), here we can view our result "on-the-fly"
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