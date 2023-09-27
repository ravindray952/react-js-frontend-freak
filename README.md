# react-js-frontend-freak

<h1>video 1</h1> //////////////////////////////////////////////////////////////////////////////////////////////////////////frontend frek

import "./styles.css";
// import {Component}  from "react";
function Greeting ({name,greeting = "Morning"}) { 
     return <h1>Good {greeting} {name}</h1>;
   }
export function App () {
    return (
    <div className="App"> 
      <Greeting name="Vishal"  greeting="Morning"/>
      <Greeting name="ReactJS"  greeting="Afternoon" />
    </div>
  );
}

props////////////////////////////////////////////////
import "./styles.css";
// import {Component}  from "react";
function Greeting (props) { 
     return <h1>Good {props.greeting} {props.name}</h1>;
   }
export function App () {
    return (
    <div className="App"> 
      <Greeting name="Vishal"  greeting="Morning"/>
      <Greeting name="ReactJS"  greeting="Afternoon" />
    </div>
  );
}

/////////////////////////////////////////////////////////////////////////////////counter app  using react js /////////////////////////////////
app.js  

 function Counter(){
    let count = 0;
    const handleIncrement =()  => {
      console.log("do increment the count")
    }
    
     const handleDecrement = () => {
       console.log("do increment the count")
     }

    return (
      <div>
         <h1>{count}</h1>
       <div>
     <button onClick={handleIncrement}>Increment</button>  
     <button onClick={handleDecrement}>Dercrement</button>
     </div>
 </div>
    )
}

export default Counter;

///////////////////////////////////////////////////////////////////counter app update the number only background
  function Counter(){
    let count = 0;
    const handleIncrement =()  => {
        count = count + 1;
      console.log(count)
    }
    
     const handleDecrement = () => {
       count = count - 1;
       console.log(count)
     };

    return (
      <div>
         <h1>{count}</h1>
       <div>
     <button onClick={handleIncrement}>Increment</button>  
     <button onClick={handleDecrement}>Dercrement</button>
     </div>
 </div>
    )
}

export default Counter;


////////////////////////////////////////////////////////////
index.js////
import { StrictMode } from "react";
import { createRoot } from "react-dom/client";

import Counter from "./App";

const rootElement = document.getElementById("root");
const root = createRoot(rootElement);

root.render(
  <StrictMode>
     <Counter/>
  </StrictMode>
);
































<h1>video 2  : usestate</h1>           //////////////////////////////////////////   counter app

import {useState} from "react";
const App = () => {
  const [count,setCount] = useState(0);
  const increment = ()  => {
    setCount((preCount) => preCount + 1)
  }; 
     return (
       <div className="App">
         <p>You clicked {count} times</p>
         <button onClick={increment}> onClick Me</button>
       </div>
     );
};

export default App;


///////////////////////////////////////////////////////////////////////////////////////////
form//////////////////// given  for update name///////////////////////////////////////////////////////////////////




import {useState} from "react";

const App = () => {
  const [Person,setPerson] = useState({
    name: "Vishal",
    role:"Frontend developer"
  });

  const handleSubmit = (e) => {
      };
  return (
    <div className="App">
        <form onSubmit={handleSubmit}>
          <input type="text"/>
          <button>Update Name</button>
          </form>
       <p>Person Name: {Person.name}</p>
       <p>Current Role: {Person.role}</p>
    </div>
  );
};
export default App
/////////////////////////////////////////////////////////////////////////////////////////////////////////
/////////////////////////////////updated name code //////////////////////////////////////////////////////////////
import {useState} from "react";

const App = () => {
  const [Person,setPerson] = useState({
    name: "Vishal",
    role:"Frontend developer"
  });

  const handleSubmit = (e) => {
     e.preventDefault();
     setPerson((preState)=>({...preState,name:e.target[0].value }));
      };
  return (
    <div className="App">
        <form onSubmit={handleSubmit}>
          <input type="type"/>
          <button>Update Name</button>
          </form>
       <p>Person Name: {Person.name}</p>
       <p>Current Role: {Person.role}</p>
    </div>
  );
};
export default App





