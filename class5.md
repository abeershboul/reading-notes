### Thinking in React

## What is the single responsibility principle and how does it apply to components?

### It mans that each component should be responsible for doing only one thing?

## What does it mean to build a ‘static’ version of your application?

###  means that it displays the UI but it is not interactive.

### Once you have a static application, what do you need to add?

### We should add interactivity.

### What are the three questions you can ask to determine if something is state?

1- What are the three questions you can ask to determine if something is state?

2-Is it passed in from a parent via props
 3- Does it remain unchanged over time?

## How can you identify where state needs to live?

* Identify every component that renders something based on that state.

* Either the common owner or another component higher up in the hierarchy should own the state.

* ommon owner or another component higher up in the hierarchy should own the state

### What is a “higher-order function”?

#### functions that can operate on other functions like taking them as arguments 

### Explore the greaterThan function as defined in the reading. In your own words, what is line 2 of this function doing?

 creates a new function to compare between numbers

 ### Explain how either map or reduce operates, with regards to higher-order functions

 ##### Map transforms the array after applying a 
 function to the contents of the array and then return a new array with the updated values.

 ### Things I want to know more about

#### when to use higher order function

