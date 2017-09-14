# React-Intro-Challenges

React Intro challenges starter project.

## Challenges

Open the [example](./index.html) in a browser and a text editor. 
Read the source code and compare it to the notes here. Then work your way 
through the challenges. 

- [Example React Components Intro](./index.html)

## The Sample Code

The sample code contains two Components: Title and Clock. These are used in the example to create 
a simple clock. 

- Title - A simple component that displays a text string in an H1
- Clock - A smart component that owns and updates a timer, and displays the time in a Title. 

Near the end of the page there is a call to ReactDOM.render(). ReactDOM keeps track of your 
components in a virtual DOM and renders this to the page.

## Challenges 

To start the challenges copy the file `index.html` in this folder. Solve the challenges by 
adding your code solutions to this file. This file has all of the boilerplate React 
code set up. You can open this file in any browser to test your solutions. 

**Try these challenges.**

1. Make a component that displays a title and a subtitle.
  - Pass the title string and subtitle string into the component as props.
  - Use this new component to display:
    - title: "React Timer"
    - subtitle: "Counts in seconds"
    - Bonus: Did you reuse the existing Title component as a subcomponent? 
    The Title component can be the title of the in your new component. 
    - Bonus: add some CSS to style the title and subtitle in the new component.
      - Hint: Assign class names to JSX with `className="my-class"` instead of `class="my-class"`
2. Make a timer that counts down from 10 to 0.
  - Start by making a new component. You can use the existing Clock component 
  as a starting point. This component displays the time by updating the time 
  every second. Notice setInterval() in the constructor calls the tick method().
  The Clock component defines a state with a property: date. This holds the date/time. 
  When state change the component will redraw. Your Timer component will need to
  define a count on state, decrement the count on each tick. 
3. Make a timer that counts down from any value to 0.
  - You'll want to pass in the starting count as a prop where the component is created.
  Inside the component get this value from props in the constructor.
    - Bonus: Set a default count of 10 in cases where the starting count is undefined.
    - Bonus: The timer counts to 0 then heads into negative numbers. Make your timer return to the
    starting count after it reaches 0.
4. Add a property to the state of the timer that determines whether the timer is running or not. 
  You can call this something "on" or "isRunning". 
  - The timer should only increment when the "isRunning" value is true. 
  - This new property should be added to state. 
  - Set the initial value for isRunning via props. 
  - Bonus: Assign an initial value when isRunning is not passed into the component via props. 
  - Test your work by making two timers on the page. One should be running and the other not. 
5. Make a new component that is a Stopwatch. The Stopwatch is a Timer with a stop/start button. 
  - The Stopwatch should count like the Timer but you should be able to start and stop it by 
  clicking the button.
    - The button should use onClick, something like this: 
```
<button onClick={ () => {
  this.startStop(); // Call a method on your component here
} }>start</button>
```
   - Bonus: The label changes to say start when the Stopwatch is stopped and Stop when the 
    Stopwatch is running. 
    - Bonus: Build this component by composing other components. To make this work the 
    `isRunning` state should be held by the parent component and passed down to the child 
    components via props. The button can be built as a simple component, it's state held
    by the parent component.
6. Make a timer that displays a message while the timer is running, and displays another 
  message when the timer reaches 0. Hint: Use state to hold the messages. 
7. Make a list that displays information. Define an array of objects. Pass this into your component 
  via props. Transform the array into an array of JSX with Array.map(). 
  - Bonus: Define a simple component for each list item. Give it at least two properties to display. 
  Reuse your title and subtitle component here. 
  - Bonus: Make a list of timers each with a start/stop button. 
  - 
8. Make a counter. It should have an up and down button, and a display to show the count. Clicking 
  the up button adds 1 to the count, clicking the down button subtracts 1 from the count. 
  - Bonus: You reused one or more of your other components. 



