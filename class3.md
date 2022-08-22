# Map function and Passing Functions as Props
**This class talks about how to use the map function and the spread operato**
## What does .map() return?
### returns a new array as a result 
## If I want to loop through an array and display each value in JSX, how do I do that in React?
### Using the map function to loop through the array 
##  Each list item needs a unique ____.
### key
## What is the purpose of a key?
### identify  item ,change and delete
## What is the spread operator?
### The spread operator is a useful and quick syntax for adding items to arrays, combining arrays or objects, and spreading an array out into a function’s arguments.
## List 4 things that the spread operator can do.
### Adding an item to a list ,Using Math functions,operator to combine two arrays,combine two objects into one
## Give an example of using the spread operator to combine two arrays.
#### const array1 = [1,2,3]
const array2 = [4,5,6]
const combinedArray = [...array1,...array2]
combinedArray = [1,2,3,4,5,6]

## Give an example of using the spread operator to add a new item to an array.
### const item = [1]
const array = [1,2,3,...item]
## Give an example of using the spread operator to combine two objects into one
#### const object1 = {name: "omar"}
const object2 = {age: 4}
const combinedObject = {...object1,...object2}
combinedObject = {name: "omar", age: 4}



## In the video, what is the first step that the developer does to pass functions between components?
###  functions with the state

## 2. In your own words, what does the increment function do?
###  loop through an array of objects and increase the count for a specific object
## How can you pass a method from a parent component into a child component?

### Using {this.iten}
##  How does the child component invoke a method that was passed to it from a parent component? 
### calling the method as a props inside a method
## Things I want to know more about

### aboute react-bootstrap
