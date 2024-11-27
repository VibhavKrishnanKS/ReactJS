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
  * so whenever we need to change something in the UI, we have to change the state of the object (we update something that is called as the state)
  * UseState() - This is a function in react which return an array
  * Then we destructure the Array according to the code above 
    * At the first position of the array we have the **advice** - which is the value of the State
    * Second value is a **Setter Function** which we can use to update the piece of the function - **setAdvice**