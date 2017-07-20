## Chapter 5: Prototypes

### Summary
The `[[prototype]]` linkage is a property reference on one object that points to another object. This linkage is particularly useful in property/method lookups. Linkage of many such objects forms a `[[prototype]]` chain.

### Lessons
* `Object.prototype` is the last stop for every ` [[prototype]]` chain and defines methods such as `.toString(), .valueOf(), .hasOWnProperty() ` available to all objects by default.

+ `new` is just an indirect way of creating two objects that are linked to each other. `Object.create()` is a direct way.

+ Shadowing of a property/method up the `[[prototype]]` chain will not occur if :
        * The method up the chain is a setter.
        * If the property is set as read only.
Shadowing methods introduces complexity and so is generally discouraged. Behavior delegation is a better option.

* The `.prototype` object has a non-enumerable property `.constructor` on it which is a reference to the function that created it. A constructor in JS is any function called with `new` infront of it.

* Delegation should be an internal implementation not exposed directly to the API.  It should be hidden inside a function.
