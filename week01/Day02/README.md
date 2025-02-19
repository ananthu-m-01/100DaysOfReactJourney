# Day 2
## Styling React Application

Inline Styling
```jsx
function Header(){
    const style = {
        color:"red",
        fontSize:"50px",
        textTransform:"uppercase"
    }
    return(
        <h1 style={style}>Heading</h1>
    )
}
```
external styling
```jsx
import React from "react"
import './index.css'
function App(){
    return(
        <div>
            <h1 className="header">Heading</h1>
        </div>
    )
}

```css
/* index.css */
.header {
    color: blue;
    font-size: 24px;
    text-align: center;
}
```
## Passing and Receiving Props

## What are the uses of Props in React
- Props are used to pass data from parent component to child component
- Essential tool to configure and customize components(like function parameter)
- With props parent components control how child component look and work
- Anything can be passed as props : Single values,arrays, objects, functions, even other components also
Parent component
- Props are immutable! This is one of the React strict Rule

```jsx
function Menu(){
    return(
        <h1>MENU</h1>
        <Product
          productName="Mobile"
          price = "40000"
        />
        <Product
          productName="Laptop"
          price = "920000"
        />
    )
}

```
Child component

```jsx
function Product(props){
    return(
        <div>
            <h1>{props.name}</h1>
            <h2>{props.price}</h2>
        </div>
    )
}
```

## Profile Card

As a Part of 100Days of React i build a simple ProfileCard React app. You can visite ProfileCard (Repository) to see my react project which i have been completed on the day2 of 100 Days of React Challenge.

### Technologies used in the Profile Card Project
- React vite
- Components and Props
- External Css Style
- Google font : Poppins

## The Rules of JSX

- JSX works essentially like HTML, but we can enter  "Java script mode" by using {} (for the attributes)
- we can place Javascript expressions inside {}. 
- Statements are not allowed `(if/else,for,switch)` 
- A Piece of JSX can only have one root element.If you need more, use `<React.Fragment>` (or the short `<>`)

## Differences between JSX and HTML

- className instead of HTML's class
- htmlFor instead of HTML's for
- Every tag needs to be closed
- CSS inline styles are written like this : ``{{<style>}}``(to reference variable and then an object)
- All event handlers and other properties need to be camelCased. Example :`onClick` or `onMouseOver`
