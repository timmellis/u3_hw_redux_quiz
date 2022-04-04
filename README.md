# Redux Quiz

<img src="https://chriscourses.com/img/blog/redux/redux.jpg" height="400px"/>

## Getting Started

- Fork and Clone

## Questions

1. What is Redux?

```
Redux is a framework that extends React and allows for a new (more robust?) way to manage state variables across the entire web application.
```

2. What packages do we install to use Redux?

```
We install both 'react-redux' and 'redux'
```

3. In your own words, describe the flow of how Redux is used to manage state.

```
Redux manages state by creating a Store where all saved state information is kept, and then gives access to that Store at the highest level (src/index.js) By sandwiching the <App /> call in the Provider tags, (like we did with Router) the Store is then shared with any and all components through App.js. 
```

4. What do we use in order to manage different pieces of state?

```
WE can manage different pieces of State from the Store. which is controlled via  store/index.js
```

5. What do we use to perform an update to state?

```
To perform updates, we create Actions that specify what Type and payload information should be passed through each Action, and then pass those actions to Reducers that process and perform updates to the Initial State.
```

6. How do we access state from Redux?

```
We map all of the State values and Actions to the "props" variables that are native to React components. We can then access them within the component as we would any other prop.    
```

7. In your own words, describe how to set up Redux for a React App.

```
Ok, yikes, let's see. Here we go: 
- We create the React App, and install 'react-redux' and 'redux'. 
- In the 'src' directory, we create a new directory 'store', and a new file '/src/store/index.js'
- In src/store/index.js, we import the {createStore} functionality from redux, (as well as {combineReducers} if we plan to use more than one). We will need to import those Reducers, and follow the syntax from the boilerplate example to create the Store and combine the Reducers, if needed.    
- In 'src/index.js', we import {Provider} from 'react-redux' and sandwich our <App /> inside of <Provider store={store}> tags which is passed the 'store={store}' parameter. We can also initialize the Redux Dev Tools here.
- In 'src/store/reducers/' we create a [TypeOf]Reducer.js file and create the initialState object, creating all of the key/value pairs we will need to pass. We also create a Reducer function that will handle the State and Action calls from other components. These will end up being used very much like our {useState, setUseState} pairs from React, only we can manage all of them at once via a switch/case block or other logic-flow block of code. 
- In 'src/actions/', create an 'Actions.js' file that templates out each action (function), including its "type" and what values it should be passed through as its 'payload'.
- For encapsulation's sake, make a new file in '/store' called 'types.js' that tracks the string values of each 'type', and import into actions/Actions.js.
-  From here, we are generally ready to go. We can create React Components where we import {connect} from react-redux, and then we can import all of the Actions we created in Actions.js. We then map the State values and Actions to "props" and grab them just like any other React prop value. Calling the Actions allows us to update and manipulate the data stored in the Initial State (in the Store).  
```

## Submission

Pull Request due by **9AM EST** following the [PR Submission Guidelines](https://github.com/SEI-R-2-22/template_pull_request).
