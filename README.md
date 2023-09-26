# react-js-frontend-freak
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
          <input type="type"/>
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





