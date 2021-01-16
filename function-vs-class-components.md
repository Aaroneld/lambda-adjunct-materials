
# Functional Components vs. Class Components 

In Javascript functions and classes are units of abstraction which allow us to encapsulate groups of data and the operations we perform on them. This is helpful because it allows us to break big problems into smaller sub problems each of which can then be focused on in isolation. This makes solving them easier and is a fundamental programmatical tool. Throughout the years the React library has leveraged these abstractions as a method by which to make the creation of client-side applications easier to manage and more efficient. For React these abstractions are called components and they essentially break up an web application into chunks (an app becomes a collection of pages, a page becomes a collection of its parts, etc...) 

Initially React used classes to represent these component structures, recently however The React library has moved to representing components as functions. These two different methods of representation accomplish the same goal but, go about acheiving it in different ways. Below is a table comparing the difference between the two.  

<table>
  <tr>
    <th width=700>Functional Components</th>
    <th width=700>Class Components</th>
  </tr>
  <tr>
    <th colspan=2>Declaration </br> 
      <sub> Demonstrates how to initialize components before building them out </sub>
    </th>
  </tr>
  <tr>
        <td>
            <pre>
                <code>
    import React from 'react';
    </br>
    function MyComponent(){
    </br>
        return ()
    }
                    </code>
            </pre>
        <span>or</span>
        </br>
         </br>
        <pre>
            <code>
    import React from 'react';
    </br>
    const MyComponent = () => {
    </br>
        return ()
    }
            </code>
        </pre> 
        </td>
     </br>
    <pre>
    <code>
    <td>
    <pre><code>
    import React from 'react' 
</br>
    class MyComponent extends React.Component { 
</br>
      render(){
        return ()          
      }
    }
    </code>
    </pre>
    </td>
  </tr>
   <tr>
    <th colspan=2>State Management </br> 
      <sub>How data is persisted and changed</sub>
    </th>
  </tr>
  <tr>
            <td>
            <h3>Initializing State</h3>
        </br>
            <pre>
                <code>
    import React, { useState } from 'react';
    </br>
    function MyComponent(){
        </br>
        const [someState, setSomeState] = useState(initialValue);
        </br>
        return ();
    }
                </code>
            </pre>
        </br>
        <h3>Accessing State</h3>
    </br>
        <pre>
            <code>
    import React, { useState } from 'react';
    </br>
    function MyComponent(){
    </br>
        const [someState, setSomeState] = useState("initialValue");
    </br>
        return &ltp&gt{someState}&lt/p&gt
    }
            </code>
        </pre>
        <h3>Changing State</h3>
    </br>
        <pre>
            <code>
    import React, { useState } from 'react';
    </br>
    function MyComponent(){
    </br>
        const [someState, setSomeState] = useState(0);
    </br>
        const handleClick = e => {
        </br>
            setSomeState(someState + 1);
        }
    </br> 
        return &ltbutton onClick={handleClick}&gtAdd One&lt/button&gt;
    }
            </code>
        </pre>
        </td>
  </tr>
   <tr>
    <th colspan=2>Lifecycle Methods</br> 
      <sub>Introducing change at specific points in time</sub>
    </th>
  </tr>
  <tr>
    <td>
       yolo
      <pre><code>yolo</code></pre>
    </td>
  </tr>
  <tr>
      <th colspan=2>Passing Props</br> 
      <sub>Communication between components</sub>
    </th>
  </tr>
  <tr>
    <td>
       yolo
      <pre><code>yolo</code></pre>
    </td>
  </tr>
</table>
