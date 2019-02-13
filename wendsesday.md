# Welcoe To React Day 4

### Today we are going talk about React Lifecycles

#### Our learning Objectives will be:

    1. Deeper understanding of React lifecycles
    2. Using Lifecycles to aid in usability
    3. Brief discussion of Refs in React
    4. Solidifying what we have covered so far

We'll Talk about which methods we can call `setState()` in each method and which methods we cannot? If we Have Time we will get into React Router...Woot Woot!



```javascript

componentWillMount(){
    //initialize variables
}

componentDidMount(){
    //call our api
}

componentDidUpdate(prevProps, prevState, snapshot) {
    // If we have a snapshot value, we've just added new items.
    // Adjust scroll so these new items don't push the old ones out of view.
    // (snapshot here is the value returned from getSnapshotBeforeUpdate)
    if (snapshot !== null) {
      const list = this.listRef.current;
      list.scrollTop = list.scrollHeight - snapshot;
    }
  }

componentWillUnmount(){
    //destroy the things
}
```
