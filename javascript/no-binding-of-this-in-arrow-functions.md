# No binding of this in arrow functions

An arrow function does not create its own this context, so this has its original meaning from the enclosing context. Thus, the following code works as expected:

```javascript
function Person(){
  this.age = 0;

  setInterval(() => {
    this.age++; // |this| properly refers to the person object
  }, 1000);
}

var p = new Person();
```

### Source

- [Arrow functions](https://goo.gl/dc8ZSv)