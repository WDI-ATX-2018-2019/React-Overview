# Welcome To React Day 2

### Today we will be covering the basics of state and props and how to deal with forms in react. 
    
    
##### Our Learning Objectives will be:
    1. Controlled Components
    2. State vs Props
    3. Lifting state
    4. Container Components
    5. Functional and Class Components
    6. Stateless vs Stateful Components
    
Hope you have fun!!!

```javascript
class extends Form extends Component {
    state = {
        username : '',
        password : ''
    }

    handleChange = () => {
        this.setState({
            [event.currentTarget.name] : event.currentTarget.value
        })
    }

    handleSubmit (event) {
        event.preventDefault()
        this.props.login(this.state.username)
    }
    render() {
        return(
            <form >
                <input type='text' name="username" placeholder="username" onCahnge={this.handleChange}/>
                <input type='password' name="password" placeholder="password" onCahnge={this.handleChange}/>
                <input type='submit' value="Submit" />
            </form>
        )
    }
}
```
 