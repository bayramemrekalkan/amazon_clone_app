# <center> π¨ AMAZON CLONE APP π¨ </center>

## π© To get started letβs make a new folder named "amazon_clone_app" and open it. As soon as you are in the folder, right click and select "Open With Code"

## π» Go to terminal, install and setup React app π
```bash
npx create-react-app .
```

## π΄ Here's how this works π
πΉ <b>npx</b> is a part of <b> npm (Node Package Manager)</b> except npx runs a remote script instead of installing it locally.

πΉ This is done so that you always have the latest version of React installed in your project.

πΉ <b>"create-react-app"</b> is the name of the remote script and <b>β.β</b> specifies that we want the script to make a React project in the <i>SAME FOLDER</i> and not make a new folder for it, if you had to make a new folder name, you could just provide the name of folder instead of β.β and it would make a folder for you.

## π» Now that we have our React App installed, now we can start it. In the terminal type the following command. This command will start the React App π
```bash
npm start
```

## π Delete three nonrelevant files from the "src" folder from the React App π

    - App.test.js
    - logo.svg
    - setupTests.js

## π© Go to "App.js" and remove the following line from your code π
```javascript
import logo from β./logo.svgβ;
```

## π© Also remove everything under the first "div" element from your "App.js" file. Youβre code should look like the following π
```javascript
import React from "react";
import "./App.css";
function App() {
    return <div className="app">React App</div>;
}
export default App;
```

## π Now letβs cleanup the "CSS" files a bit. Go to "App.css" and remove all the contents of your file.

## π© Now go to "index.css" and add this piece of code on the top. This will get rid of the margin and padding of the page. π
```css
*{
 margin: 0;
 padding: 0;
}
```

## π Now we have our React project perfectly set up. Now we can start making the Amazon Clone.

# π’ 1-SETTING UP THE REACT ROUTER

- A very important thing to consider in a React app is the <b>navigation <i>(moving from one page to another)</i></b> of the users. Since React is a single page application, it doesnβt support multiple routes by default.

- But the node packages come to our save. Thereβs a package named <b>react-router-dom</b> which allows us to create routes for our React project. Not a lot complicated. Setting up is one time, and then whenever you add a new page, you just need to inform the Router. Donβt worry we will cover that in depth here!

## π» Go to terminal to install "react-router-dom" π
```bash
npm install react-router-dom
```

## π For reference [click here](https://v5.reactrouter.com/web/guides/quick-start).

## π© Creating Component π

- Once itβs installed, now letβs get our hands dirty and write some actual code. Letβs make a new component.

- To make a component, simple make a new file. We call it <b>Home.js</b> under "src" folder for our case. The convention is that the first letter of a component must be in <b>capitals</b> π’

- Also to make life easier, go ahead and install a Visual Studio Code extension named [ES7 React/Redux/GraphQL/React-Native snippets](https://marketplace.visualstudio.com/items?itemName=dsznajder.es7-react-js-snippets). This extension will make the boiler plate for React components without you being typing the code all by yourself.

## π© Home.js π

- Letβs go in "Home.js". 
- Just type in <b>βrfceβ</b>, hit Enter while on βrfceβ
- This will autocomplete the React boiler plate for you.
- Now letβs change the class of the div element provided us to βhomeβ.
- We follow BEM convention while styling our components.
- <b>BEM Convention</b> helps our CSS and JSX organized for us to read later, and everything becomes easy to keep track of.
- Letβs just add some text there for now, letβs say Hello. The code on the <b>Home.js</b> file now should be π

```javascript
import React from "react";
function Home() {
   return <div className="home">Hello</div>;
}
export default Home;
```

## π© App.js π

- If you see the browser, you will not see anything because we havenβt prepared our entry point <b>App.js</b> yet.
- So letβs open the file and start setting up the <b>React Router</b>.
- First of all, we need to import the dependencies.
- Import them using the following code at the top of <b>App.js</b> π

```javascript
import { BrowserRouter, Routes, Route } from "react-router-dom";
```

- Once youβve done importing the code, you can now use React Router in your file.
- Now that we have imported React Router, letβs configure React Router according to our needs. Use the below code in your <b>App.js</b> π

```javascript
import React from "react";
import "./App.css";
import { BrowserRouter, Routes, Route } from "react-router-dom";
import Home from "./Home";

function App() {
return (
    <>
        <div className="app">
            <BrowserRouter>
                    <Routes>
                        <Route path="/" element={<Home />} />
                    </Routes>
            </BrowserRouter>
        </div>
    </>
);
}
export default App;
```

- Our motive is to have <b>Home</b> component to be rendered on the default route that is β/β.
- To use the <b>Home</b> component, we need to import it, so we imported it at the top.
- We need to wrap the entire app into the Router component, so that every component is a part of Router and has access to the Router.

### π© We now have the Router set up. Letβs go ahead and make the Amazon Navbar

# π’ 2. CREATING THE NAVBAR

## π» We are going to use a package for icons, and we need Material Icons to use them. So open your terminal and write the following command π
```bash
yarn add @material-ui/core
```
- Once you installed the dependencies, you can use it to display SVG icons which are provided by <b>Material UI</b>.
- Material UI is a very popular UI library for React which has a lot of prebuilt components just as icons which makes life easier.

## π© Create a New Component π "Header.js" and "Header.css" under "src" folder

## π’ In each component, we will follow the same steps. We have to initialize the component boiler plate using βrfceβ and follow the BEM convention and include the CSS file and update the class names π
```javascript
import React from 'react'

const Header = () => {
  return (
    <div className='header'>Header</div>
  )
}

export default Header
```

## π© We need to include "Header Component" in "Router" so that we can actually display it. In "App.js" where you mentioned Route for "/" route, letβs include the "Header" component in it too. Your updated route should look like this π
```javascript
<Route path="/">
  <Header />
  <Home />
</Route>
```

## π’ Remember you place Navbar before the Home component, because the Amazon Navbar is always at the top π

## π© Go back to "Header.js" and start setting up the layout of our classic Amazon Navbar π
```javascript

```