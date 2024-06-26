# Quick Start

## Creating and nesting components

React apps are made out of components.  A component is a piece of the UI (user
interface) that has its own logic and appearance.  A component can be as small
as a button or as large as an entire page. 

React components are JavaScript functions that return markup: 
```
function MyButton() {
    return (
        <button>I'm a button</button>
    ); 
}
```

Now that you've declared MyButton, you can nest it into another component: 

```
export default function MyApp() {
    return (
    <div>
        <h1>Welcome to my app</h1> 
        <MyButton /> 
    </div>
    ); 
}
```

Notice that MyButton starts with a capital letter. That's how you know it's a
React component. React component names must always start with a capital letter,
while HTML tags must be lowercase. 

The `export default` keywords specify the main component in the file. 

## Writing markup with JSX

The markup syntax you've seen above is called JSX.  It is optional, but most
React projects use JSX for its convenience.  All of the tools we recommend for
local development support JSX out of the box. 

JSX is stricter than HTML.  You have to close tags like <br />. Your component
also can't return multiple JSX tags.  You have to wrap them into a shared
parent, like a <div> or an empty <> wrapper. 

## Adding styles

In React, you specify a CSS class with className.  It works the same way as the
HTML class attribute:  

```
<img className="avatar" />

/* In your CSS */ 
.avatar {
    border-radius:  50%; 
}
```

## Displaying data

JSX lets you put markup into JavaScript.  Curly braces let you "escape back"
into JavaScript so that you can embed some variable from your code and display
it to the user.  For example, this will display `user.name`:  

```
return (
    <h1>
        {user.name}
    </h1>
); 
