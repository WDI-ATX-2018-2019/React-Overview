# Woot Woot Today Is The Last Day of React

## Congratulations on Making it this far

### Today we will talk about Redux

> ##### Redux is a global state management tool that can be used with React. It is very powerful for large applications however it is highly obtuse and abstract, so I will not be assigning any Redux homework to you however I will provide you with some resources on how to implement this in any project you are working on, and a tutorial so that you can practice it for the on the Job!

## [Redux Docs](https://redux.js.org/)

[HERE IS A TUTORIAL FOR REDUX](https://medium.com/@notrab/getting-started-with-create-react-app-redux-react-router-redux-thunk-d6a19259f71f) I wont say it's quick lol.

### There are several piecest that we need to know about in Redux

### 1. Store
--- 
   This is the central place where our global state is kept. This state should be immutable. Meaning when we update the global state we create a new piece of state and leave the old piece alone. This lets us keep track of the state and move backwards in time if we have to.

### 2. Actions
--- 
   This what triggers the Redux State Lifecycle for example the click of a button or a call to an external REST API. We will have Action Creators wich are the events that occur within javascript, and then we will have the actions them selves which should be pure in nature while passed to the reducer.

### 3. Reducers
--- 
   These are funcitons that take inital state and an action and reduce it to the new state. `(state, action) => newState` These though they might seem abstract are intended to be PURE FUNCTIONS without any side effects. 

### 4. Dispatch
---
    This is where the actions are dispatched our store and our Reducer.

### 5. View
---
Well...the view is our react app. This is where our events that fire Actions Live.





## Here is a highlevel diagram of the lifecycle.
---
![Diagram](https://camo.githubusercontent.com/9de527b9432cc9244dc600875b46b43311918b59/68747470733a2f2f73332e616d617a6f6e6177732e636f6d2f6d656469612d702e736c69642e65732f75706c6f6164732f3336343831322f696d616765732f323438343739302f415243482d5265647578322d657874656e6465642d7265616c2d6465636c657261746976652e676966)
---


```javascript
//==> ACTION <==
const ADD_LETTER = "ADD_LETTER"

//==> REDUCER <==
function wordReducer(state = "", action) {
  switch (action.type) {
    case "ADD_LETTER":
      return state + action.letter
    case "RESET":
      return ""
    default:
      return state
  }

  //==> ACTION CREATORS <==
  function addLetterWithDispatch(text) {
    const action = {
      type: ADD_LETTER,
      text
    }
    dispatch(action)
  }
    //without dispatch
  function resetAction() {
    return "RESET"
  }
}
```
