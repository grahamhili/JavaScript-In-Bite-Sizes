Function Arguments
------------------

* Function Arguments are __untyped__

```javascript
"use strict";

function Add(a, b, c) {
    return a + b + c;
}

console.log(Add(1, 2, 3));      // returns 6
console.log(Add('a','b','c'));  // returns abc
console.log(Add('2','b',3));    // return 2b3
```

* Function Arguments can be empty. Empty arguments become __undefined__ in the function.

```javascript
"use strict";

function Add(a, b, c) {
    return a + b + c;
}

console.log(Add(1, 2));     // returns NaN
console.log(Add(1, '2'));   // returns 12undefined
```

* If more function arguments are passed to a function the extra arguments are __ignored__.

```javascript
"use strict";

function Add(a, b, c) {
    return a + b + c;
}

console.log(Add(1,2,3,4,5,6,7));      // returns 6
console.log(Add('a','b','c','d'));    // returns abc
console.log(Add('2','b',3,'xxx'));    // return 2b3
```

* Functions have a special object called __arguments__

```javascript
"use strict";

function Add() {
    console.log(arguments);
    console.log('Arguments Length= '+arguments.length)
    return 0
}

console.log(Add(1, 2, 3, 4, 5, 6, 7));
// { '0': 1, '1': 2, '2': 3, '3': 4, '4': 5, '5': 6, '6': 7 }
// Arguments Length= 7


console.log(Add('a', 'b', 'c', 'd'));
// returns { '0': 'a', '1': 'b', '2': 'c', '3': 'd' }
// Arguments Length= 4

console.log(Add());
// returns 0
// Arguments Length= 0
```
