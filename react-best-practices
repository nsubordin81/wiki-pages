# ES6 conventions:

- avoid using var in ES6 use let and const
- use strict should be declared so that this doesn't default to window, it is undefined instead.
- native js functions run in the C++ context of the javascript engine which is a ton faster, so don't write your own implementation of map() or use jquery's for example, use the ones that are provided by the language.
- don't use jquery. Just don't.
- ES6 arrow functions create anonymous wrapper functions for every iteration of a loop so they are not good candidates for thunks that are evaluated in every iteration of a loop <-- understand. 
- useful property of arrow functions, they use lexical scope this instead of call site this and are hoisted in to the ES6 class constructor, which saves you a lot of headache when writing handler functions for local state.   
- babel will bind all of your anonymous functions for you. 

# React conventions:

- jsx is not inline html, it is transplied into js and you can look at the js that webpack generates when debugging
- you don't have to worry about target vs. currentTarget when handling events in react. Due to synthetic event handling, across all browsers react will handle events the same way and you don't have to worry about catching events too deep in the DOM tree because React will take care of that for you.
- convention for react component naming: capital camel case for custom components, lowercase for native components
- use redux for shared application state and not state that is local to a component. 
- state objects should be flat, nested state is more difficult to work with during event handling
- when updating a parent component's props in a child component through state, create a copy of the props into a state object instead of assigning props directly. If props are on the rhs, you are providing a reference to the child to mutate the parent's props which is bad.
- don't use refs unless you have to they manipulate the DOM
- avoid using dangerouslySetInnerHTML because it loads content from the database directly into the markup of your page which bypasses react's cross site scripting protection. 

# React Instruction and resources:
- react (and redux) are built on the design best practices that we are becoming familiar with through use of other languages and functional programming: pure functions, immutable state, and having a single source of truth
- zones are a useful way to improve stack traces, profile and debug asynchronous javascript code. https://www.youtube.com/watch?v=3IqtmUscE_U

Things that are common accidents to do: 
- rendering from props instead of state,
- passing prop to child when yo meant to pass state. 
- Invoking a function when you meant to pass a function reference
- Typo in the event handler name
- Forget to inherit from React.Component
Checking object references instead of ids
Accidentely using the props of the instance instead of parameter props

Things that can do but you don’t always want to: 
You can put an anonymous wrapper function inline into the event handler property of a jsx element, but be careful, if this is in a loop it will be called every time. 
Named exports youi can use curly braces and then name what you are importing to the file
