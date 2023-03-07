![Logo-nav](https://s3.ap-south-1.amazonaws.com/kalvi-education.github.io/front-end-web-development/Kalvium-Logo.png)

# Kalvium Lab | REACT - MASTER OF HOF

## Learning Goals

In this exercise, the goal is to apply various higher order functions in react:

- when and how to setup react in your application,
- learn map, filter and reduce

Whenever you create a first significant change, you should make your first commit.

3. Follow these [guidelines to add, commit and push changes](https://github.com/FACEPrep-ProGrad/general-guidelines-labs-project-builders.git).

### Introduction

In this exercise, you will try to work with various higher order functions.

**You should use map, filter and reduce**

create a new react app using the following command

```
npx create-react-app hof
cd hof
```

Now go to your app.js and remove the unnecessary code. Your app.js should be looking similar to the this.

```
import React from 'react';
import HigherOrderComponent from './components/HigherOrderComponent';
import './App.css';

function App() {
  return (
    <div className="App">

    </div>
  );
}

export default App;
```

Now create a folder called components inside the src folder and create a component called HigherOrderComponent.js file. Once you create it you are good to go.

So let's get started!
Check below to see the overall output: You will be trying to replicate this

![Image description](https://s3.ap-south-1.amazonaws.com/kalvi-education.github.io/front-end-web-development/rendering-lab-all.png)

### PROGRESSION 1 | DEFINE THE STATE

Your task in this iteration is just to create an array of objects inside the state. To do this, let's go to our HigherOrderComponent.js and inside the class try to define the constructor and the state.
Just remember you need to define the super constructor before defining the state. Your code should look something like this.

```
  constructor(){
        super();
        this.state = {
            userData: [
                { id: '1', name: 'Joe', user_type: 'Developer', age:31, years:11 },
                { id: '2', name: 'Hill', user_type: 'Designer', age:26, years:4 },
                { id: '3', name: 'John', user_type: 'Teacher', age:24,years: 2},
                { id: '4', name: 'Sam', user_type: 'Entreprenuer', age:58,years:25},
                { id: '5', name: 'Jack', user_type: 'Designer', age:43, years: 18}

            ]
        }
    }

```

You're ready to move to the next iteration. :raised_hands:

### PROGRESSION 2 | LIST ALL ITEMS

Now we have defined our data to be used. Your task in this iteration is to display all the elements from userData.
Your output should be looking like this.

![Image description](https://s3.ap-south-1.amazonaws.com/kalvi-education.github.io/front-end-web-development/rendering-lab-displayAll.png)

**Remember to use map function to display all the details**

Code Snippet for reference

```
// display all items
renderItems = () => {
    const data = this.state.userData;
    const mapRows = data.map((item) => (
        <React.Fragment key={item.id}>
            <li className="list-elements">
                {/* Passing unique value to 'key' prop, eases process for virtual DOM to remove specific element and update HTML tree  */}
                <span>Id: {item.id}</span>
                <span>Name : {item.name}</span>
                <span>User Type: {item.user_type}</span>
           </li>
        </React.Fragment>
    ));
    return mapRows;
};

```

Now the most important step, You need to return the value to the render method so that the output get's displayed in the container.

```
render() {
        return (
        // instead of a parent div tag we can also use React.Fragment
          <React.Fragment>
            <h1>Display all items</h1>
            <div className="display-box">
            <ul>{this.renderItems()} </ul>
            </div>
          </React.Fragment>
```

If you do the above, you still can't see the output. Do you know why it is because you need to add your component to your app.js file.

![Image description](https://s3.ap-south-1.amazonaws.com/kalvi-education.github.io/front-end-web-development/rendering-lab-structure.png)

If you get the above output, you can ensure that the react is completely setup in your system.

### PROGRESSION 3 | LIST ALL DATA BASED ON USERTYPE

Your output should like this. In this iteration you should filter the userData based on the `UserType`.
**Note: Please use map and filter**

![Image description](https://s3.ap-south-1.amazonaws.com/kalvi-education.github.io/front-end-web-development/rendering-lab-usertype.png)

### PROGRESSION 4 | FILTER ALL DATA STARTING WITH THE LETTER `J`

Filter all names starting with the letter J.
**Note: Please use map and filter**

Your output should like this.
![Image description](https://s3.ap-south-1.amazonaws.com/kalvi-education.github.io/front-end-web-development/rendering-lab-letter-J.png)

### PROGRESSION 5 | FILTER DATA BASED ON AGE

In this progression, Filter the data based on the age. The age should be `greater than 28 and less than or equal to 50`.
**Note: Please use map and filter**

Your output should like this.
![Image description](https://s3.ap-south-1.amazonaws.com/kalvi-education.github.io/front-end-web-development/rendering-lab-agefilter.png)

### PROGRESSION 6 | FIND THE TOTAL EXPERIENCE OF THE DESIGNERS

In this progression, you need to find the total years of experience of the designers.

**Note: Please use map, filter and reduce**
Your output should like this.
![Image description](https://s3.ap-south-1.amazonaws.com/kalvi-education.github.io/front-end-web-development/rendering-lab-total-years.png)

## Summary

If you managed to do it, good job! :trophy:

We are proud of you!

Happy Coding Kalvium ❤️!
