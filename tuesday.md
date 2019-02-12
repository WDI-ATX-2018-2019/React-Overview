# Welcoe To React Day 3

### Today we are going to cover AJAX, `fetch()`, `componentDidMount()`, async/await in React!

#### Our learning Objectives will be: 
    1. Makeing Ajax calls with `fetch()` in react
    2. Using Async/Await and or promises for syncronicity in react
    3. Understanding some of the basic Lifecycle Methods
    4. Understanding why and when to use `componentDidMount()`
    5. rendering better UI with lists

If we have time we will do some React review and get even more practice!

```javascript
componendDidMount() {
  getCrimes = async () => {
    try {
      const crimes = await fetch('https://data.cityofchicago.org/resource/crimes.json');
       if (!crimes.ok) {
          throw Error(response.statusText);
       }
      const crimesJson = await crimes.json();
      this.setState({crimes: crimesJson});
    } catch (err) {
      console.log(err, 'error in catch block')
      return err
    }
  }
}

```