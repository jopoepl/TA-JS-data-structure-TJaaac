1. What will be the output and explain the reason.

```js
let obj = { name: 'Arya' };
obj = { surname: 'Stark' };
let newObj = { name: 'Arya' };
let user = obj;
let arr = ['Hi'];
let arr2 = arr;
```

Answer the following with reason after going through the above code:

- `[10] === [10]` //false - reference value for arrays are diff even if the value is the same 
- What is the value of obj? // { surname: 'Stark' };
- `obj == newObj` //false obj has got the new value so its not the same as newObj
- `obj === newObj`// false - same as above
- `user === newObj` // false - different reference values
- `user == newObj` // false - same as above
- `user == obj` // true - same reference value 
- `arr == arr2` // true - same reference value
- `arr === arr2` //true - same as above

2. What's will be the value of `person1` and `person2` ? Explain with reason. Draw the memory representation diagram.

<!-- To add this image here use ![name](./hello.jpg) -->

```js
function personDetails(person) {
  person.age = 25;
  person = { name: 'John', age: 50 };
  return person;
}
var person1 = { name: 'Alex', age: 30 };
var person2 = personDetails(person1);
console.log(person1);
console.log(person2);
```

Basically, personDetails would simply overwrite any object with new object elements - { name: 'John', age: 50 }. So output will always be this irrespective of the input.

As for person 1, its already defined and we are just logging that details. 



3. What will be the output of the below code:

```js
var brothers = ['Bran', 'John'];
var user = {
  name: 'Sansa',
};
user.brothers = brothers;
brothers.push('Robb');
console.log(user.brothers === brothers); // true 
console.log(user.brothers.length === brothers.length); // true 
```

// both are true because arrays and objects use reference value and any changes made would reflect immediately in an assigned variable. 