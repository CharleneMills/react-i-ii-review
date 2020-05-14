### Remember

Answer these on your own, then compare answers as a group

1.  What are props?

A: Data being passed from Parent to Child.
Its an object that allows us to pass data from parent to child.

-----------------------------


2.  How do you pass props from a parent to a child?

A: Set it on the parent, then google it or look at the slides.

Through JSX attributes. Assign attributes to the compoennt with the prop name and value.

```jsx

<ChildComponentWithProps propName={this.state.propValue} usernameProp={this.state.username}/>

```

-----------------------------------


3.  How do you access props from a class-based child component?

A: Look at the slides

```jsx
{this.props.whatever}
```

4.  How do you access props from a functional component?

A: without the 'this', and put 'props' as a parameter in the child function


5.  How do you bind a function to a parent component so that it can be passed to a child?

A: can use the arrow function in your methods - can cause memory leaks if used in lots of passing down and not as secure.
OR
A: you use this.myMethod = this.myMethod.bind(this) - in the constructor



### Understand

Discuss this question in pairs if you have a 4-person group

6.  What's happening in this component?

```jsx
import React, { Component } from "react";

class Queue extends Component {
  constructor(props) {
    super(props);

    this.state = {
      questions: []
    };

    this.askQuestion = this.askQuestion.bind(this);
    this.answerQuestion = this.answerQuestion.bind(this);
  }
  askQuestion(newQuestion) {
    const questions = [...this.state.questions, newQuestion];
    this.setState({ questions });
  }
  answerQuestion(index) {
    const questions = [...this.state.questions];
    questions.splice(index, 1);
    this.setState({ questions });
  }
  render() {
    <div className="queue-container">
      <h1>The Queue</h1>
      <h3>{this.state.questions.length}</h3>
      <h3>questions need answers</h3>
      <Student askQuestion={this.askQuestion} />
      <Mentor answerQuestion={this.answerQuestion} />
    </div>;
  }
}
```

A: It a que system for people to ask questions. The container is showing how many are in the que. Then under questions that need answers it is showing the questions that need answering or allowing students to ask new questions, and same for the mentors.





### Apply

Try these on your own, but work together if you start to get stuck.

7.  Using the `Queue` component above, create a `Student` component that can add a question as a string and a `Mentor` component that can remove a question from the array.

### Analyze, Evaluate, Create

Discuss these questions as a group

8.  In the Queue component above, why are we holding state in the Queue component instead of Mentor or Student?
