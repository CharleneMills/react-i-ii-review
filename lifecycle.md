### Remember

Use https://reactjs.org/docs/react-component.html#the-component-lifecycle and http://projects.wojtekmaj.pl/react-lifecycle-methods-diagram/ to answer these on your own then compare answers as a group

1.  Each component has several `lifecycle methods` that you can override to do what?

A: Increase and Customize the performance of our app.


2.  What are the 3 categories of lifecycle methods? (these are the headings from the first link)

A: Mounting, Updating, UnMounting


3.  What are the names of the 5 commonly used lifecycle methods? (these are in bold in the first link)

A: Constructor, Render, componentDidMount, componentDidUpdate, componentWillUnmount




### Understand

Discuss this question in pairs if you have a 4-person group

4.  What's going on in this code?

```jsx
import React, { Component } from "react";

class Mentor extends Component {
  componentDidUpdate() {
    console.log("Dwight saved the day!");
  }
  render() {
    return (
      <div>
        <h1>Dwight Schrute</h1>
        <h2>{this.props.questions.length}</h2>
        <h3>questions to answer</h3>
        <button onClick={this.props.answerQuestion}>Answer a question!</button>
      </div>
    );
  }
}
```


A: 

1) Constructor Runs
2) Render Runs
3) If Render Runs again componentDidUpdate





### Apply

Try these on your own, but work together if you start to get stuck.

5.  Update the `Mentor` component above so that the message that is currently being console.log'd is displayed below the number of questions to answer instead.
