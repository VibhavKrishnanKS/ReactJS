# 2. Building Our first react app

1. A Component is React is just really a function that's it 
```jsx
  return (
    <div>
      <h1>Hello World!!</h1>
      <button onClick={getAdvice}>Get Advice</button>
    </div>
  );
```
The Functions return something calledd **JSX** - which is a syntax that looks like HTML 

2. **State** - This is the most fundamental concept of React
```jsx
import { useEffect, useState } from "react";

export default function App() {
  const [advice, setAdvice] = useState("");
  const [count, setCount] = useState(0);

  async function getAdvice() {
    const res = await fetch("https://api.adviceslip.com/advice");
    const data = await res.json();
    console.log(data.slip.advice);
    // In order to update the value that is seen in the
    // console log insid the UI we use the useState
    setAdvice(data.slip.advice);
    setCount((c) => c + 1);
  }

  useEffect(function () {
    getAdvice();
  }, []);

  return (
    <div>
      <h1>{advice}</h1>
      <button onClick={getAdvice}>Get Advice</button>
      <Message count={count} />
    </div>
  );
}

function Message(props) {
  return (
    <p>
      You have read <strong>{props.count} </strong>
      pieces of advice
    </p>
  );
}
```
  * so whenever we need to change something in the UI, we have to change the state of the object (we update something that is called as the state)
  * UseState() - This is a function in react which return an array
  * Then we destructure the Array according to the code above 
    * At the first position of the array we have the **advice** - which is the value of the State
    * Second value is a **Setter Function** which we can use to update the piece of the function - **setAdvice**
  * Also we can use UseEffect() - In order to save the state so that when you reload the state stays the same(we have to read on this)

## How to add different components in React
  * Also we have illustrated what is meant by **Props** which is like a parameter which you u pass to the function and you receive it on the other function using the **props** object


3. Another finding which i did 
```jsx
import { useState } from "react";

export default function App() {
  const [Vibhav, Kumar] = useState("");

  async function getAdvice() {
    const res = await fetch("https://api.adviceslip.com/advice");
    const data = await res.json();
    console.log(data.slip.advice);
    // In order to update the value that is seen in the
    // console log insid the UI we use the useState
    Kumar(data.slip.advice);
  }

  return (
    <div>
      <h1>{Vibhav}</h1>
      <button onClick={getAdvice}>Get Advice</button>
    </div>
  );
}
```
* you can assign any variable name to the two positions of the array and based on that you have to change accordingly
