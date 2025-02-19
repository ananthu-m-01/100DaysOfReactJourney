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

```
```css
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

As a part of **100 Days of React**, I built a simple **ProfileCard** React app. You can visit [ProfileCard (Repository)](https://github.com/ananthu-m-01/Profile-Card) to see my React project, which I completed on **Day 2** of the **100 Days of React** Challenge.


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

## Rendering List
- `map()` method is used to rendering the list dynamically
```jsx
import React from  "react"
const data = [
    {
        name: "John Doe",
        skills: "JavaScript, React, Node.js",
        salary: "$80,000"
    },
    {
        name: "Jane Smith",
        skills: "Python, Django, Machine Learning",
        salary: "$90,000"
    },
    {
        name: "Alice Johnson",
        skills: "Java, Spring Boot, Microservices",
        salary: "$95,000"
    },
    {
        name: "Bob Williams",
        skills: "C++, Data Structures, Algorithms",
        salary: "$85,000"
    },
    {
        name: "Charlie Brown",
        skills: "HTML, CSS, JavaScript, Bootstrap",
        salary: "$70,000"
    },
    {
        name: "David Clark",
        skills: "Angular, TypeScript, RxJS",
        salary: "$88,000"
    },
    {
        name: "Emma Davis",
        skills: "Swift, iOS Development, UI/UX",
        salary: "$92,000"
    },
    {
        name: "Franklin Miller",
        skills: "Kotlin, Android Development, Firebase",
        salary: "$87,000"
    },
    {
        name: "Grace Hall",
        skills: "PHP, Laravel, MySQL",
        salary: "$78,000"
    },
    {
        name: "Henry Wilson",
        skills: "DevOps, AWS, Docker, Kubernetes",
        salary: "$110,000"
    }
];

function Office(){
    return(
        <ul>
            {data.map(item => <Employee employeeObj={item} key={item.name}/> )}
        </ul>
    )
}

function Employee(props){
    return(
        <li>
            <h3>{props.employeeObj.name}</h3>
            <h4>{props.employeeObj.skills}<h4>
            <h4>{props.employeeObj.salary}</h4>
        </li>
    )
}

```

## Conditional rendering with && 

```jsx
function Menu(){
    const hour = new Date().getHours();
    const openHour = 12;
    const closedHour = 22;
    const isOpen = hour >= openHour && hour<= closedHour;
    return(
        <div>
        {isOpen && <p>We are Open until {closedHour} :00</p>}
        </div>
    )
}
```
```jsx
function Menu(){
    const employees = data;
    const numberOfEmployees = employees.length;

    return(
        <h1>Details of Employees</h1>
        {
            numberOfEmployees > 0 && (
            <ul>
                {
                    employees.map((employee) =>(
                        <Employee employeeObj={employee} key={emploee}>
                    ))
                }
            </ul>    
        )}
    )
}
```
## Conditional rendering with Ternaries

```jsx
function Menu(){
    const employees = data;
    const numberOfEmployees = employees.length;

    return(
        <h1>Details of Employees</h1>
        {
            numberOfEmployees > 0 ? (
            <ul>
                {
                    employees.map((employee) =>(
                        <Employee employeeObj={employee} key={emploee}>
                    ))
                }
            </ul>    
        ): <p>No Data available </p>
        }
    )
}
```

```jsx
function Menu(){
    const hour = new Date().getHours();
    const openHour = 12;
    const closedHour = 22;
    const isOpen = hour >= openHour && hour<= closedHour;
    return(
        <div>
        {isOpen ? <p>We are Open until {closedHour} :00</p> : <p>Closed</p>}
        </div>
    )
}
```
