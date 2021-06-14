---
layout: post
title:      "Intro to the useState Hook"
date:       2021-06-14 14:58:33 +0000
permalink:  intro_to_the_usestate_hook
---


The react ecosystem is currently undergoing a migration towards a more functional
programming paradigm. The react team has realeased a new set of tools to interact
with the DOM and use state in your apps. Hooks are functions that allow programmers
to "hook" into react features, without the need for class components. This, along
with the drive towards a more functional design pattern, is being done to simplify
code increasing maintainablity, and making it easier to implement new features.

## Hooks, Hooks, Hooks

React, as well as most of the popular libraries apart of the typical app stack, have
implemented their own hooks. React Router has it's useParams and useLocation hooks.
Redux built the useDispatch and useSelector hooks to replace the connect component
for react class components. Hooks are the future, and the sooner you learn how to
use them the better off you'll be as the industry moves towards the new standard
set by the react devs.

## The React State Hook

Let's take a look at the hook provided by the react library used to initialize
and mutate state at the functional level. This is how a simple class component
will initialize state:

    class Example extends React.Component {
      constructor(props) {
        super(props);
        this.state = {
          count: 0
        };
      }

      render() {
        return (
          <div>
            <p>You clicked {this.state.count} times</p>
            <button onClick={() => this.setState({ count: this.state.count + 1 })}>
              Click me
            </button>
          </div>
        );
      }
    }
    // this example was taken from the react documentation

As a flatiron student, you are probably already pretty familiar with this syntax.
State is initialized in the constructor function, and then accessed by `this.state.count`,
and mutated by `this.setState({ count: etc.. })`. In the following example, we
have a functional component that initializes, accesses, and mutates the component
state with the `useState()` hook imported from the react library.

    import React, { useState } from 'react';

    function Example() {
      // Declare a new state variable, which we'll call "count"  
      const [count, setCount] = useState(0);
      return (
        <div>
          <p>You clicked {count} times</p>
          <button onClick={() => setCount(count + 1)}>
            Click me
          </button>
        </div>
      );
    }
    // this example was taken from the react documentation

If you are unfamiliar with react using hooks, you might be surprised to see state
being used in a functional component. Prior to hooks being introduced to react,
only class components were able to use state. Now functional components can use
state too, making it easier to build simpler apps, with fewer lines of code, that
are vastly more readable. It is important to understand however that the `useState()`
hook still only sets and augments component state. To use redux, you will either
need to use the hooks provided by the redux library or continue using the connect
component to conect your app to the redux store. So what is `useState()` for?

Dan Abramov, a name you should already be familiar with if you are using react professionally,
popularized the design pattern followed by the flatiron curriculum. In this [article](https://medium.com/@dan_abramov/smart-and-dumb-components-7ca2f9a7c7d0),
he describes the presentational and container component paradigm, where the state
and application logic are seperated from the components that the user actually sees
and interacts with. But if you visit that article now, you'll notice that Dan has
added an update. He sees react hooks as a better solution to the problems posed by
a production environment. There will be times where a component requires state, but
a container component can't be justified, and the redux store state should not have
to store that data. A great example of this is registration or login, which are the
first two components I transitioned to use hooks. Sometimes it is better to have
the state, logic, and ui all grouped together into one component.

## Start Using Hooks Today

React hooks are not going anywhere. If anything, they are taking over. While it is
to keep your knowledge of class components fresh, most new apps are going to built
using a functional pattern with hooks, and most of the class components you see will
be in legacy code. So get started with hooks now.
