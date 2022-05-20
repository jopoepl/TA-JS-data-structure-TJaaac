```js
let user = {
  name: 'Arya',
  sibling: ['Robb', 'Ryan', 'John'],
};
let allBrothers = ['Robb', 'Ryan', 'John'];
let brothersCopy = user.sibling;
let username = user.name;
let newUser = user;
```

1. Memory representation

- Create the memory representation of the above snippet on notebook.
- Take a photo/screenshot and add it to the folder `code`

![Hello](./hello.jpg)

<!-- To add this image here use ![name](./hello.jpg) --> 

2. Answer the following with reason:

- `user == newUser;` // true - since user is an object it has value by reference which is shared with the newUser
- `user === newUser;`// again true, because the reference values will be exact 
- `user.name === newUser.name;`//true because both have the same assigned values
- `user.name == newUser.name;`// again true
- `user.sibling == newUser.sibling;` true - they have the same values
- `user.sibling === newUser.sibling;` true
- `user.sibling == allBrothers;` false - while they may seem to have same values, their reference values will be different
- `user.sibling === allBrothers;` false - reason same as above
- `brothersCopy === allBrothers;` false
- `brothersCopy == allBrothers;` false
- `brothersCopy == user.sibling;` true - because we have defined this way
- `brothersCopy === user.sibling;` true - reason same as above 
- `brothersCopy[0] === user.sibling[0];`true - because they have same reference values
- `brothersCopy[1] === user.sibling[1];`true - reason same as above
- `user.sibling[1] === newUser.sibling[1];`true
