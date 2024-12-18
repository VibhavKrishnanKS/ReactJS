# Side Notes for the Pure React Video 

**NOTE** - We are going with the concept of **PURE WAY OF USING REACT**


1. **React.dev** - This is the official website of react (In order to view the documentations)
2. Go To the Learn Part -> 
  2.1 Installation -> 
  2.2 Search for the heading **Try React Locally** -> 
  2.3 Click the Hyperlink **download this HTML page** -> 
  2.4 Add the below two scripts in order to add React to your HTML
  ```jsx
    <script src="https://unpkg.com/react@18/umd/react.development.js"></script>
    <script src="https://unpkg.com/react-dom@18/umd/react-dom.development.js"></script>
  ```
  Now you have actually included react into the project
  1. The first one is the **CORE REACT LIBRARY** - This works with 
    1.1 Components
    1.2 States
    1.3 All the React Stuff
  2. The Second one is the **REACT DOM** - which renders all the React components into the dom


**REMEMBER**  - React is completely based on **Components**
**Component** - This is basically just a function which starts with an upper case like below 
1. We Can't return a JSX Code here - because we don't have the tool that renders **JSX -> Javascript**
2. So we use the **Create Element function** here
```jsx
<body>
  <div id="root"></div>
  <script src="https://unpkg.com/react@18/umd/react.development.js"></script>
  <script src="https://unpkg.com/react-dom@18/umd/react-dom.development.js"></script>
  <script>
    function App() {
      // This is coming from the first import which gives us the below React object
      return React.createElement("header");
    }
  </script>
</body>
```
Initially at this stage we won't be having the component rendered to the page -> Cause we didn't tell react to do it yet 
3. 
