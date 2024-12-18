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
    const root = ReactDOM.createRoot(document.getElementById('root'));
    root.render(React.createElement(App));
  </script>
</body>
```
After adding the extra above lines in the code, we get the header element added inside the **div(id=root)** element
![Rendered React Component](./1.%20Rendered%20Header%20Component%20.png)

4. The createElement() function doesn't acccept only the name of the HTML element -> It totally takes three elements as parameters   
  4.1 The Three elements are   
    A. Name of the HTML element 
    B. props -> here it is **null**    
    C. Third Argument -> This is the **children of this element** (Here as a third element we just write a string which is **Hello React**)
```jsx
<body>
  <div id="root"></div>
  <script src="https://unpkg.com/react@18/umd/react.development.js"></script>
  <script src="https://unpkg.com/react-dom@18/umd/react-dom.development.js"></script>
  <script>
    function App() {
      // This is coming from the first import which gives us the below React object
      return React.createElement("header", null, "Hello React!!");
    }
    const root = ReactDOM.createRoot(document.getElementById('root'));
    root.render(React.createElement(App));
  </script>
</body>
```
![Hello React Serving As a Child Node](./2.%20Hello%20React%20Child%20Node.png)  
Here the **Hello React Serves as a Child Node**(where the **header element serves as a parent node**)

5. **One of the Reason why we don't write Pure React in a Real Time Developement Environment**    
Before we would directly write HTML -> cause we used JSX to write the code   
we don't need to write the weird thing which we did above   
We Would directly write it as HTML basically  
But that approach doesn't work here   

6. 




