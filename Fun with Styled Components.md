# Fun with Styled Components & it's working, 


## Styled Components

So styled components is pretty popular but for some reasons I never liked it one of the reason was that there was no autocompletion,
Turned out that you can install the style component syntax highlighter and it will give you the autocompletion in the template literal

Also I was bit sceptical about using it with react native but again it turned out that it is better and doesn't impact too much on the performance part

It seemed that rather than writing the style sheet of react-native it's better if we just use styled component.

So Rakesh was telling me about all this and I agreed with him, this is a better choice after lot of discussion.

### Using it with useCallback

So then we thought what if we use some dynamic variables and state variables with the styled-component
Then we had to move that style component inside the react function and if we do that it means
 everything will be calculated again and again on render so so we tried using use callback but it returned a function.

Then the magic happened report everything inside the usecallback hook and return it from there and then we just called it outside.
It seemed like magic and everything worked perfectly we tested lot of times there were no rerendering it was only getting recalculated only on the state changes provided of dependency array.

So this seeing the great achievement for us 🥳

### How it works ?

So now the question started arising that how does the style component works

We started doing some diggings and turns out that if we define a function and put template literal after that function it will be called and all the the value inside template literal will be passed as an array with all the strings.

Another thing was that the styled-components give few methods for the particular component are element.
Then we started digging the source code of style components and we found out that they just have a string of every component which is 
styleable in react native and what they are doing is just splitting it with the spaces and they are just looping through it and creating methods on their function.


Then we went ahead and tried creating something like this, then we kind of built our on mini style components for JavaScript and we could not do bunch of stuff with it because obviously there are thousands and thousands lines written for the style component and all the passing which happens with the template literal being passed as a string so we had to stop going further.
But yeah it was a lot of learning and fun to create something like this and
 I hope you enjoyed this
