# The Modern React Bootcamp
## Section 1: A taste of React
**React** its a popular, powerful front-end framework/library Developed by and sponsored by Facebook. React makes it easy to make reusable "view components" encapsulating HTML and LOGIC into a class, often make it easier to build modular applications.
## Components: 
Component let you split the UI into independent, reusable pieces, and think about ech piece in isolation.
- The building blocks of React
- Pieces of UI & view logic
## Section 2: Introducing JSX
JSX syntax allows us to combine our UI with our javascript logic directly on our javascript file, so rather than having a separate template file in HTML that we then call upon in our javascript we can look at a single component and directly see what it actually result it.  
- JSX isn's legal javaScript
- It has to be transpiled to JavaScript
- It can be use using Babel.
Basic Rules: 
- Have an explicit closing tag `<b></b>`
- Be explicity self-closed. `<input name="msg />`
- Cannot leave off that / or will get sytax error
## Section 3: Props and More
**Properties** aka PROPS allows us to make our components more customizables.
- Props are for configuring your component, for passing data in from a parent that help customize or configure a child component
- Properties are inmutable 
## Section 4: Introducing Create React App
Basic comands
```
npx create-react-app my-app
npm start
```
## Section 4: Pokedex
See at https://github.com/pauligarcia8/Pokedex-game
## Section 5: Introducing State
- Internal data specific to a component.
- Data that change over time!
A great way to think about state is to think of games, fos instance chess. At any point in time, the board is in a complex state. Every new move represents a single discrete state change.
If your component have a state you need tThe basic standard React constructor, wich is the next:  
constructor(props) {  
    super(props);  
    this.state =  {  
            /* values we want to track */  
        };
    }
}

- constructor takes one argument, props
- you must call super(props) at start of constructor, wich "register" your class as a React Component
- Inside the instance methods, you can refer to this.state just like you did this.props
### this.setState() 
is the built-in React method of changing a component's state. There's a couple of options for how we call it, the first on is:
1. an object:
this.setState({ playerName: 'Matt', score: 0}). 
- Can call in any instance method except the constructor
- Takes an object state describing the state changes
- Patches state object - keys that you didnt specify dont change
- Asynchronus
    - The component state will eventually update
    - React controls when the state will actually change, for performance reasons.
- Componenets re-render when their state changes
### React Events
State most commonly changes in direct response to some event. In react, every JSX element has built-in attributes representing every king of browser event. They are camel-cased, like *onClick* and take callback functions as event listeners.
`<button onClick={function(e){alert('You clicked me');}}>Click Me!</button>`
