# React
React is a frontend Javascript library. Is is an open source component-based library that is in charge of developing the application's view layer.
Since its initial release in 2013, React has become one of most popular javascript libraries for UI development. It is easier to reason about and debug, and its capacity to effectively alter the user interface in response to data changes.

## Advantage of React
* React is easy to learn.
* The syntax of react is much like HTML which allow developers to create templates with detailed documentation.
* We can migrate one version to another.

## Create React App
Create-React-App is a tool developed by Facebook for creating and building React application with minimal setup. It allows developer to quickly set up a new project with a basic file structure and a development server, Without having to manually configue webpack or babel. CRA also provides a set of script and tools that make it easy to test, build, and deploy React applications.
By using Create-React-App developer can focus on writing code for their application instead of spending time configuring the development environment.

```
create-react-app name of project
```
you can use the following command to install the create-react-app package globally on your machine if you prefer not to write npx each time you start a new project.
```
npm install -g create-react-app
```
Once you create-react-app is installed, you create a React application as follows:
```
create-react-app name-of-project
```
```
cd myapp/
```
Then start your project by using follo9wing commands:
```
npm start
```
Now local host 3000 should host your react application.

## New Root API
** Legacy Root API
** New Root API

## Introducing the new root API
A root in react refers to the top-level data structure that renders a tree. In React 18, we will have two root APIs:
**Legacy root API** and 
**New root API**
### Legacy Root API.
The legacy root api is the existing API called with reactDOM.render method. It will create a root running in legacy mode, which is similar to usage in eact version 17. If we are using reactDOM.render() in your react 18 app, we will definitely see the below issue.

AJSX element is converted into regular javascript object during compilatin so that it can be used to construct a genuine DOM element .

The reason in ReactDOM.render is no longer supported in react 18.
Earlier, we used to render the component in below way:
```
ReactDOM.render(<NavBar/>, document.getElementById('root'))
```
** The render() method of react-dom package is considered legacy starting react-dom version 18.
** The method is replaced with createRoot() method that is exported from react-dom/client.
** The createRoot() method taked the root elements as parameters and creates a react root.

## New Root API
createRoot() is a new method instoduced in react 18 that allows you to create a separate root for a react tree outside of the main react DOM tree. it take a single argument, which is a reference to an existing DOM element. It returns a new root object that has a render() method for rendring react components into the specified DOM element.

call createRoot to create a React root for displaying content inside browser DOM element.
### old way to do
```
impprt ReactDOM from 'react-dom';
const rootNode = document.getElementById('root');
ReactDOM.render(<App />; rootNode);
```

### New way to do
```
import ReactDOM from 'react-dom/client';

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<App />);
```
React will create a root for the domNode, and over managing the DOM inside it. After we've created a root, we need to call root.render to display a react component inside of it:

```
root.render(<app />)
```
An app fully build with react will usually only have one createRoot call for its root component. A page that uses "sprinkles" of react for part of page may have as many separate roots as needed.

## JSX
Jsx stands for javascript XML. It is a syntax extenstion for javascript that allow you to write HTML-like elements in our javascript code . it is used in react a describe the structure and content of a component.

One of the main benefits of JSX is that it makes it easy to create and manipulating the structure of a components. 
```
const name =<h1> hello Bachoo</h1>

```
A JSX elements is converted into a regular javascript object during compilation so that it can be used to construct a genuine DOM elements . For instance, the javascript generated from the jsx code above might be as follow :
```
const name = React.createElement("hi", null,"hello bachoo");
```
Basic difference between JSX and HTML
```
<ul>
<li>Pw skills
<ol>
<li>web development</li>
<li>data science</li>
<li>java with DSA</li>
</ol>
</li>
<li>physic</li>
<li>chemistry</li>
</ul>
```
## output
<ul>
<li>Pw skills
<ol>
<li>web development</li>
<li>data science</li>
<li>java with DSA</li>
</ol>
</li>
<li>physic</li>
<li>chemistry</li>
</ul>
 Nested JSX must retur a single element that wrap all other levels of nested elements, which we'll refer to as the parent element:
 ```
 <div>
 <h1> what is skill </h1>
 <p>lorem text</p>
 <p> lorem dummy text</p>
 </div>
 ```
 ##output
 <div>
 <h1> what is skill </h1>
 <p>lorem text</p>
 <p> lorem dummy text</p>
 </div>

All html attributes references in JSX becomes camelcase this way onclick event become onclick and onchange- onChange.
### Browser can't read JSX
JSX is a comnination of html and javascript so it is not supported by browser. So, a transpiler called Babel converts the JSX into pure javascript. The browser understand the ode and execute it. Browser can't read JSX because there is no inherent implementation for the browser engine to read and understand them.

## Why JSX 
With help of jsx, we can write html code with javascript.React does not employ the createElement() method; instead, JSX elements are used to create HTML elements. As a result,JSX faciliates the writting and addition of html components in eact. A transpiler called babel.js will conver JSX to javascript on the browser.
Babel is a library that converts JSX to pure javascript and newest javascript to previous versions.

## Embedding JS expressions in JSX
Since JSX is a javascript extension enclosed in curly brackets'{}'. This enables you to add dynamic elements to your JSX. This can be string, a number, a boolean, an object, or even an array.

## CDN 
A CDN is content delivery network, is a distributed network of servers that work together to provide fast and reliable delivery of digital content, such as images, vedios, web pages, and other static or dynamic assests to end user accross the globe.

The main purpose of CDN is to reduce latency and improve the speed of content delivery by caching and distributing content across multiple geographic lovcations, so that the content has to travel, reducing the time it take to load the content and improvinf the user experience.

CDNs also provide other benefits such as improved scalobility increased rliablity and avaliability and better security by offloading traffic from origin servers and protecting against DDoS attacks and other types of theads.

Overall, A CDN can be an essentials tool for organization that need to delivery content quickly and efficiencyto a global audience, such as e-commerce sites, media companies and other conetnt heavy websites.
