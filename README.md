This project are my notes on learning REACT.  It's largely from the Pluralsight course "React:Getting started"

COURSE OVERVIEW
- pre-reqs are just basic javascript

THE BASICS
- Introduction
  - using Hooks and Class components

- Why REACT
  - A javascript library for building user interfaces
  - Frameworks vs libraries
  - good for building ios mobile apps
  - Created and supported by Facebook

- React's Basic concepts
  - components (functions or class)
  - Reactive updates
  - Virtual views in memory. Generate HTML using javascript
  - JSX is not HTML

- Your First React Component
  - We'll create a Button with a numeric label that increases each time you click on it
  - webtool for course: jscomplete.com/playground.  This was built with React
  - type javascript into the playground
     eg.
     document.getElementById('mountNode').innerHTML = 'Hello';
 - works with: React, ReactDOM,  JSX,  ES2015+
 - Load React devtools extensio in your browser
 - https://jscomplete.com/playground/rgs1.1
 - JSX is a javascript extension
 - Babel  is a javascript compiler that turns JSX into REACT API calls
 - Everything that gets displayed in REACT is a Component

- Your first React hook
  - the useState function is known as a 'hook' in REACT
  -

- You firs one way data flow
  - This is all about defining variables and functions in a parent function and passing them down to child function
  - responsibility isolation

- Component re-usability
  - changing button value and creating more values

- Tree Reconciliation in action
  -use the setInterval function to display how react behaves to regeneration of a page.   It doesn't overwrite text placed in an input box

- Wrap UP
  - Summarize all the items above that we've learned


MODERN JavaScript CRASH COURSE
- ECMAScript and TC39
- Arrow functions
- Classes
- Promises and Async/Await


THE Github CARDS APP
- What are we building
  - Use Github's public API.  We'll use class components.  We'll create a page where we can add user handles.

- React Class Components
  - Build the general view of the App and and do some plain formatting with CSS

- Styling React components
  - learn an alterative way to style components inline with JavaScript instead of a global CSS area

- Working with Data
  - github API url to get data. api.github.com/users/gaeron
  - https://jscomplete.com/playground/rgs2.3
  - get the data from a test user in github and use it to display in your project. Save into testData object.
  - create the 'CardList' Component
  - the the ".map" javascript function of arrays to map all cards

- Initializing and Reading the State object
  - Create a simple form with a button that will be used to submit a user name.
  - We'll need to track state to fully implement input capability into the form so we begin setting up the react function to track state
  - React by default tracks state of all components in an object called 'state'
  - discussed a class constructor and the super function.

- Taking Input from the user
  - We define a state within the Form component and tract the userName within it.
  - Then in form element we leverage the react 'setState' function to read the input value from the Dom and pass it to the react state.
  - We show that we indeed can read the input by displaying it to the console

- Working with Ajax calls
  - Now We're ready to interact with the github API to download the data dynamically.
  - Instead of using the browser's native 'fetch' call we'll use the simpler 'axios' that's made available within the playground
  - Once the data is fetched we'll pass it from the form component up to the App via a function call that will chnage the state of the App component
  - Homework:
    - Add error handling as shown in his book jscomplete.com/react-beyond-basics
    - Convert all componets to functions instead of Classes
    - Track state in an individual component
  - Final code is in: jsdrops.com/rgs2.7



  THE STAR MATCH GAME
  - What are we building
    - https://jscomplete.com/react-games/star-match
    - https://jscomplete.com/playground/rgs3.1
  - Working with static markup
    - create a function to display the stars
    - avoid for/while loops in react if possible.  Use map/filter/reduce instead
    - use the random function to change number of stars
    - set the stars as a state element
  - Extracting components for reuse
    - What divs do we want to turn into a component, a react function
    - Convert button generation into a component
    - JavaScript closures.
 - View Functions State => UI
    - Create the logic to change the color of the numbers based on their sate.  Use simulation data instead of actually reading from the buttons.
    - It's often easier to define the UI logic first.
    - create a function to track state of number and pass it to the Play

- Behavior Functions : State => New State
  - Write code for the behavior that will happen once a number is actally clicked.
  - create a onNumberCLick function. This function needs to read the state and be able to change it.
  - Use .filter to re-add unselect a button that had been clicked before that was a wrong choice.
  - We now have a playable game

- Resetting the state
  - Display a 'playAgain'  button once game is over and code to signal that the game is over.  Performed this by just checking length of the available items array
  - The general flow of the code for a component follows this order:
     first:  defining the state (variables)
     second: computations based on the state
     third:  Display the UI based on all the state.
 - add a reset function to clear and reset all counters.

- Using Side Effects Hooks
  - Implement the timer feature.
  - useEffect() - This is a react hooks function as useEffect is.  It automatically triggers anytime there's a state change to the component housing it.
  - concept of side effect
  - setTimeout().
  - React re-renders every time the state changes
  - read: jscomplete.com/rgs-hoolks to learn how to fix problem with clearTimeout
  - set game to done once timer runs out or display complete if player selected all correct answers.

- Un-mounting and remounting components
  - In order to reset all component states in one shot we'll have react render a new version of the game each time.
  - This is achieved by having the main component as Game and having the StarMatch component, that is rendered ReactDOM.render, display the call to game with an individual key.  This has the effect of mounting a new instance of Game each time the project is run.

- Using custom Hooks
  - We break up the game component into smaller pieces by separating the state and the management of state into its own component.
  - The things we learned in this project were:
    - How we Initialize state
    - How to Initialize side effects
    - how to define custom Hooks
    - How to group everything together that's about managing state
    - How to use the key attribute to unmount a component and remount again to clean up side effects and give it a brand new state.
    - And leave the main element to make computations and display the UI description to reflect the state


SETTING UP A DEVELOPMENT ENVIRONMENT
- Introduction
  - Multiple Tools : APIS , Configurations, Releases
  - Multiple environments: Dev, Prod, Test
  - Different renders: DOM, SSR

- Create React APP
  - "create_react_app" is just an npm package

- Installing Environment Dependencies.

- Configuring your own Environment

- Reactful

- Structuring Component Files

- What's next
