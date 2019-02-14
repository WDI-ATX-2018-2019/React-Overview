# Welcoe To React Day 5

### Today we are going talk about React Router and HOC (Higher Order Components). This is the home Stretch for the React Section. Make Sure you voice any concerns or questions you have today before we get to project week.

#### Our learning Objectives will be:

    1. Understand and Practice React Router
    2. Be able to use Static Routes, Redirects, and Nested Routing
    3. UnderStand Higher Order Components Conceptually
    4. Use HOC and Higher Order Components to Handle Authenticating Login

```javascript
import React from "react"
import { BrowserRouter as Router, Route, Link } from "react-router-dom"

const BasicExample = () => (
  <Router>
    <div>
      <ul>
        <li>
          <Link to='/'>Home</Link>
        </li>
        <li>
          <Link to='/about'>About</Link>
        </li>
        <li>
          <Link to='/topics'>Topics</Link>
        </li>
      </ul>

      <hr />

      <Route exact path='/' component={Home} />
      <Route path='/about' component={About} />
      <Route path='/topics' component={Topics} />
    </div>
  </Router>
)
```
