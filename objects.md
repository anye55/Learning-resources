## Chapter 3: Objects

## Lessons

+ Objects are a collection of key/value pairs where the values can be accessed using the `.key` notation. Object sub-types include `function` and `array`.

+ During property access,  the `[[Get]]`operation traverses the object for the value and the object's `[[prototype]]` chain if the value is not found directly on the object. The same happens with `[[Put]]`.

+ Property descriptors such as `writable` and `configurable` can be used to manipulate object properties. Additionally, objects can have their mutability controlled using `Object.preventExtensions()`, `Object.seal()` and `Object.freeze`.

* ES6's `for .. of` can be used to loop over data structure **values** using an `iterator`. Also `enumerable` property descriptor determines whether or not  a property will show up in a `for ..in` loop.
