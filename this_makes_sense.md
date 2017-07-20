## Chapter 2: `this` All Makes Sense Now.

### Lessons

+ To resolve the `this` binding for a function, we need to understand the functions **call-site** (the location where the function is called). To understand the call-site, we need the call stack (the stack of functions called to get us to the current moment in execution.) The call-site of interest is the invocation before the currently executing function.

+  JS debugger in Chrome developer tools can be used  to determine the call stack and hence the call-site of a function.

+ The four rules for resolving `this` binding in order of precedence:
    + Called with `new`? Use the newly constructed object.
    + Called with `call()`, `apply()`, or `bind()`? Use  the specified object
    + Called with a context object? Use the centext object.
    + Default? global scope or `undefined` in `strict mode`.

+ Functions that lose their this binding can be hard bound.

+ The DMZ object protects the gobal object `window` for browsers from unintended side-effects.

+ The `this` binding of arrow functions cannnot be over-written even with `new`.
