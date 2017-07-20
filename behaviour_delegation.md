## Chapter 6: Behaviour Delegation
### Summary
Behaviour delegation  is where an object provides delegation to another object (by virtue of being created using ( `Object.create()`) for property and method lookups. The mental model for classical "prototypal" **OO** style code involves function objects with `.prototype`links to objects that delegate to each other. However, the **OLOO** style  model involves only **objects linked to other objects. **

### Lessons

+ (Design tip) In classical OO style code, state is stored in the functions and methods (behaviour) are  stored on the `.prototype` objects. Likewise, with `[[prototype]]`delegation, state is stored on the **delegators** not the **delegate** (the object the delegators delegate to).

+ Functions in JS also have a `[[prototype]]` linkage to a function object `Empty()` which they delegate to for default methods such as `call(), apply(), bind()`.

+ **OLOO** supports better the principle of separation of concerns, where creation and initialization are not necessarily conflated into the same design (author's words.)

+ Type introspection is much easier with **OLOO** because it involves only objects  and `isPrototypeOf()`is used directly.
