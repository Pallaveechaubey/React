# react-document

## Table of Content  
[What is React?](#What-is-React)

[ Advantage of React](#Advantage-of-React)	

[What is Tailwind CSS?](#what-is-tailwindcss)

[Why we are integrating tailwindcss with react project?](#Why-we-are-integrating-tailwindcss-with-react-project?)

[What is Create React app](#What-is-Create-React-app)	  

[JSX](#JSX)

[Setup for React Project](#Setup-for-React-Project)	    


## What is React?

React is a front-end Javascript library. It is an open-source component-based library that is in charge of developing the application's view layer. Since its initial release in 2013, React has become one of the most popular javascript libraries for UI development. It is easier to reason about and debug, and its capacity to effectively alter the user interface in response to data changes.

# Advantage of React

* React is easy to learn.
* The syntax of react is much like HTML which allow developers to create templates with detailed documentation.
* We can migrate one version to another.

## What is Tailwind CSS?

Tailwind CSS is like a toolbox for styling websites or apps. Instead of giving you pre-made styles for things like buttons or headers, it gives you lots of small tools (called utility classes) that you can use to style elements directly in your HTML code.

For example, instead of having a class for a big blue button, you might use utility classes to make a button big, blue, and rounded.

## Why we are integrating tailwindcss with react project?

When you use a CSS framework like Bootstrap, it gives you a bunch of ready-made styles that you can apply to things like buttons or tables just by adding certain classes to your HTML code.

But with Tailwind CSS, it's a bit different. Instead of giving you pre-made styles, Tailwind CSS gives you small building blocks called utility classes. These classes let you control things like margins, padding, colors, and more directly in your HTML code.

## What is Create React app 

* It create a new directory with the given project name and generates a basic file structure for a React.js application. the generated file structure includes the following:

* There are 3 folders in the following React boilerplate: node modules, public, and src, Read.md, package.json, gitgnore, and yarn.lock are additional files.

* node_modules: here we get all the necessary node packages of our application.
* Public
* index.html: only one html file is there in the whole application.
* manifest.json: It is applied to transform the application into a progressive web app.
* favicon.ico: It is an icon in the tab.
* src
* App.css,index.css: These are different css files.
* index.js: A file which allows to connect all the components with index.html.
* App.js: A file where we usually import most of the presentational components.
* serviceWorker.js: is used to add progressive web app features.
* setupTest.js: to write testing cases.
* package.json: it shows the list of packages the application uses.
* .gitignore: react boilerplate comes with git initiated and .gitignore allows files and folders to be ignored when committing new changes.

## JSX
Jsx stands for javascript XML. It is a syntax extension for javascript that allows you to write HTML-like elements in our javascript code. it is used in react a describe the structure and content of a component.

One of the main benefits of JSX is that it makes it easy to create and manipulating the structure of a components.
```
const name =<h1> hello Bachoo</h1>
```
A JSX elements is converted into a regular javascript object during compilation so that it can be used to construct genuine DOM elements. For instance, the javascript generated from the JSX code above might be as follows:
```
const name = React.createElement("hi", null,"hello bachoo");
```
## Basic difference between JSX and HTML
* Nested JSX must return a single element that wraps all other levels of nested elements, which we'll refer to as the parent elements.

* All HTML attributes and event references in JSX become camelCase, this way, the onclick event becomes onclick and onchange - onchange.

## Browser can't react Jsx 
JSX is a combination of HTML and JavaScript. so, it is not supported by the browser. so a transpiler called babel converts the JSX into pure javascript. Then browser understands the code and executes it. Browsers can't read JSX because there is no inherent implementation for the browser engines to react to and understand them.

## Why Jsx 
With the help of JSX, we can write HTML code with javascript. React does not employ the createElement() method; Instead, JSX elements are used to create HTML elements. As a result, JSX facilitates the writing and addition of HTML components in React. A transpiler called babel.js will convert Jsx to javascript on the browser.

### Advantages of Jsx 

* Because JSX  syntax is so similar to HTML syntax, which many developers are already familiar with it is simpler to write and read.
* It enables you to specify your whole react components using declarative syntax in a single file by using JSX elements as the component's root.
* By using attributes which are identical html attributes, it make it simples to give data to your code clean and manageable.

### Note 
* JSX must have one parent element.
### Why JSX
JSX is converted into a plain javascript object. In JavaScript, you can only return one object from a function. The same applies to JSX - If you want to return multiple Jsx tags, you need to wrap them in a parent tag.

## Ternary operation inside Jsx elements
The ternary operator can be used with JSX components to conditionally render different elements or components based on certain conditions. The ternary operator is shorthand version of if/else statement and has the following syntax :
```
Condition? true:false
```
Here is an example of ternary operators within a JSX component:
```
functionMyComponents(props){
    return(
        <div>
        {props.isLoggedIn ? <p>Welcome back!</p> : <p>please log in</P>}
    )
}
```
In this example the components receive props called isloggedin and use the ternary operator to determine whether to show a "welcome back message " or please login  message. The condition is the prop is logged in is true it will render the first element and if it is false it will render the second element .

It is worth noting that the ternary operator is more concise than an if/else statement but it can be less readable when the conditions are complex in that case is recommended to use if/else statement.

## What are HTML attributes 
HTML attributes are properties that are  used to define the characteristics and behavior of HTML elements. they are added to the opening tag of HTML element and come in the form of name-value pairs, with the name being the attribute and the value being what it set to

For example, commonly used attributes include "class", "id", "src", "href", "for" etc, and events like "onclick".

```
<div class="my-class">Hellow world </div>
```
But in react we use 'className' attribute instead of class.

Let's take another example of on click event in HTML.
In HTML we use "on click in all lower case but in react we use camel case like 'onClick " " Also in HTML, we have to put the function in quotes and invoke it by putting parameters but in React we use curly braces and the function name without parenthesis.

* In HTML a "label" is an element that can be used to provide a text description for a form element such as a text field or a checkbox. The "for" attributes of the label elements are used to associated the label.
With specific form elements typically by specifying the ID of the form element.
In react, a "label" component can be created using javascript and jsx to create and style label elements. These components can be reusable and can be used in different parts of application.

### NOTE--
We already know there are certain differences between html and jsx and one such difference that we have seen in html. In normal HTML we have for but we cannot use it in javascript since it is a reserved keyword in javascript so we use htmlFor in jsx.

 ## Introducing the new root API 
 A root in react refers to the top-level data structure that renders a tree. In React 18, we will have two root APIs: Legacy root API and New root API

### Legacy root API
The legacy root API is the existing API called the reactDOM.render method. It will create a root running in legacy mode, which is similar to usage in each version 17. If we are using reactDOM.render() in your react 18 app, we will definitely see the below issue.

AJSX element is converted into a regular javascript object during compilation so that it can be used to construct a genuine DOM element.

The reason in ReactDOM.render is no longer supported in React 18. Earlier, we used to render the component in the below way:

```
ReactDOM.render(<NavBar/>, document.getElementById('root'))
```

 The render() method of the react-dom package is considered legacy starting react-dom version 18. ** The method is replaced with createRoot() method that is exported from react-dom/client. ** The createRoot() method taked the root elements as parameters and creates a react root.

 ### New Root API
 createRoot() is a new method introduced in React 18 that allows you to create a separate root for a react tree outside of the main react DOM tree. it take a single argument, which is a reference to an existing DOM element. It returns a new root object that has a render() method for rendering react components into the specified DOM element.

call createRoot to create a React root for displaying the content inside the browser DOM element.



```
// Import ReactDOM from 'react-dom';
import ReactDOM from 'react-dom';

// Import the App component (assuming it's defined in a separate file)
import App from './App';

// Get the root DOM element where the React app will be rendered
const rootNode = document.getElementById('root');

// Old way of rendering React component
// ReactDOM.render(<App />, rootNode);

// New way of rendering React component using Concurrent Mode and createRoot
import ReactDOM from 'react-dom/client';

// Create a root instance using createRoot, passing the root DOM element
const root = ReactDOM.createRoot(rootNode);

// Render the App component inside the root
root.render(<App />);
```

## Explanation:
** Old way (ReactDOM.render()):
  - `ReactDOM.render()` is the traditional way to render a React component into a DOM node.
  - You pass the component you want to render (in this case, `<App />`) as the first argument, and the DOM node where you want to render it (in this case, `rootNode`) as the second argument.

** New way (Concurrent Mode and createRoot()):
  - With Concurrent Mode and the new createRoot API, rendering is performed asynchronously and allows for more efficient updates.
  - Instead of using `ReactDOM.render()`, you first create a root instance using `ReactDOM.createRoot()`, passing in the root DOM element.
  - Then, you call `root.render()` with the component you want to render (in this case, `<App />`).

Using Concurrent Mode and `createRoot()` is the recommended approach for rendering React components in newer applications, especially when dealing with large or complex UIs, as it can provide better performance and user experience.

# Setup for React Project

## Install node.js 
```
https://nodejs.org/en
```
## Check if the node is successfully install or not using the below command
```
node -v
npm -v
```
* Go to visual Sudio code and create a folder xyz.
* open terminal and run the below mentoned command.
```
npm create vite@latest
```
* Mention project name ex - first_project.

## select the framework
* react
* Javascript

``` 
cd first_project
npm install
npm run dev
```
## Integrate tailwindcss with react project 
```
npm install -D tailwindcss
npx tailwindcss init
```
* Go to the tailwind.config.js file and the below-mentioned to the module.exports.

```
content: ["./src/**/*.]
```

* index.css is the main CSS file of the project, add the mentioned below
```
@tailwind base;
@tailwind components;
@tailwind utilities;
```


