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
(Object.setPrototypeOf(num, arr.__proto__))
  //(Number, 0);
  
  try {
   num.push(num); // this will through an error. cannot use the push method on a primitive data type (number on this case)
  } catch(err){
   arr.push(num);
  }
```

On Chrome Developer Console:
<a href="https://ibb.co/f8anY9"><img src="https://preview.ibb.co/i53wRU/Screen_Shot_2018_08_14_at_20_47_23.png" alt="Screen_Shot_2018_08_14_at_20_47_23" border="0"></a>

Notice how it outputs just 0, a data primitive type Number. How is this possible since this method should return an object?
Well, since num isn't an object, it will not successfully set the new prototype of that object array 'arr' to the number type 'num'. 
That being said, using the try-catch method is useful to reach another solution. Declaring a different object and using it as the first operand of setPrototypeOf would be one of them. Either way, what matters is understanding the Prototypical inheritance and knowing what is an object and what isn't, in JavaScript. 



[TOP](#index)

___

## Practice Points:

[TOP](#index)

## Helpful Links

* Proto: [MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/proto)
* setPrototypeof() : [MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/setPrototypeOf)
[TOP](#index)
