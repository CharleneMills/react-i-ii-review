### Remember

Answer these on your own, then compare answers as a group

1.  What is React?
React is a javascript library which allows you to build SPA's, manages the virtual dom, and is unidirectional in flow. 

Some comparible libraries are Vue and Angular.

2.  What is create-react-app?
A package through NPM (Node Package Manager) that allows you to build a quick React App. 

A package built by facebook to facilitate building apps in react and to standardize react apps by centralizing the dependencies

3.  What is Component Based Architecture?
Architecture that breaks the organization of the SPA into seperate components. Rusuable and easy to debug

4.  What is JSX?
JavaScript Syntax Extension that can produce react elements. It uses an HTML-like syntax. 

5.  What is the virtual DOM?
A copy of the DOM that acts as a go between for the browswer and the actual DOM. It 'listens' for changes to the code allowing for only pieces of the code to be refreshed instead of the entire page.

A virtual copy of the browser DOM that React uses to identify and target changes to make in the browser DOM in a process called reconciliation. (it is stored in memory)


6.  What is unidirectional (one-way) data flow?
Data can be passed one direction (In React it passes from parent to child and not child to parent).


### Understand

Discuss these questions in pairs if you have a 4-person group

7.  Summarize what happens when you run `create-react-app my-app`
In the terminal, it creates a new "pre-packaged" react app called whatever you want to call it, in this case "my-app"

8.  Summarize the steps for forking and cloning a repo with an existing React app. How does this process differ from the process of creating a new React app on your laptop?

1) Fork
2) Clone
3) Navigate into that folder
4) Run npm i for any dependencies needed

vs

1) Create new repo
2) Create your folder structure 
3) Follow the instructions it gives you
4) If you are createing a react app then the create-react-app will install dependencies for you


9.  Explain what this code does:

```jsx
import React from "react";

const Mentor = props => (
  <div className="mentor-container">
    <h1 className={props.title === "Lead Mentor" ? "lead" : ""}>Tim Biles</h1>
    <ul>
      <li>Fort Worth, TX</li>
      <li>My email address is timbilestimbiles@gmail.com</li>
    </ul>
  </div>
);

export default Mentor;
```

Its adding a class based on a condition

10.  Explain how data is passed from a parent component to a child component.

Props

### Apply

Try these on your own, but work together if you start to get stuck.

11.  Use `create-react-app` to create a new React application called `student-directory`

12.  Use the code from `Mentor` above to create a new functional, stateless component called `User` with a list of friends. Hard code the list of friends, do not use state or props.

### Analyze, Evaluate, Create

Discuss these questions as a group

13. What are the benefits and drawbacks of using a tool like create-react-app?

14. Compare and contrast JSX with other templating options, such as those used in Angular or Vue

15. Compare and contrast one-way data flow with two-way data binding.
