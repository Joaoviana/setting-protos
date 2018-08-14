## Setting Prototypes

Setting prototypes of objects to data primitive types does not seem to work on JavaScript. 
But why?

### Index
* [Learning Objective](#learning-objective)
* [Study Snippet](#study-snippet)
* [Practice Points](#practice-points)
* [Helpful Links](#helpful-links)
___

## Learning Objective

Language Features:
* array.push() method
* Object.prototype.setPrototypeOf(obj,prototype)


[TOP](#index)

___
 
## Study Snippet

```js
let arr = [], num = 0;
(Object.setPrototypeOf(num, arr.__proto__)).push(num);

```

[TOP](#index)

___

## Practice Points:

[TOP](#index)

## Helpful Links

* Proto: [MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/proto)
* setPrototypeof() : [MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/setPrototypeOf)
[TOP](#index)
