# this
all about where you are calling the function.
needed to avoid 'uggly code' in the angular world
this == a context object bound at the time a function is called

``` javascript
"use strict"; // when included undefined, when not included get the global object/window
function whoAmI() {
    console.log(this)
}
whoAmI() 
```
``` javascript
"use strict";
let amazingObj = {
    amazingVar : 'amazed',
    function beAmazed() {
        console.log("time to be " + this.amazingVar)
    }
}

// broken
let anotherobj = {
    superSecrete: 'afdasdfasdf',
    doSomething: function () {
        utils.doCallback(500, function() {
            console.log('the secrete is ${this.superSecrete}')
        })
    }
}

// works but bat
let anotherobj = {
    superSecrete: 'afdasdfasdf',
    doSomething: function () {
        that = this
        utils.doCallback(500, function() {
            console.log('the secrete is ${that.superSecrete}')
        })
    }
}

// still ok
let anotherobj = {
    superSecrete: 'afdasdfasdf',
    doSomething: function () {
        utils.doCallback(500, function() {
            console.log('the secrete is ${this.superSecrete}')
        }.bind(this))
    }
}

// new modern way
let anotherobj = {
    superSecrete: 'afdasdfasdf',
    doSomething: function () {
        utils.doCallback(500, () => {
            console.log('the secrete is ${this.superSecrete}');
        })
    }
};
```

# prototypes
## What is prototype?
linking one object to another
prototypes are shared between all the objects
```javascript
Person.prototype.doThing(){
    console.log("did the thing");
}
```

https://git.io/vdHln

https://toddmotto.com/understanding-the-this-keyword-in-javascript