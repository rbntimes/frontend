# About this repository

# Best practices

#### Best practice lecture 3

> Avoid long parameter lists in method signatures

[Sauce](https://medium.com/@janakachathuranga/coding-best-practices-javascript-9a5f397d701b)

##### Instead of:

```javascript
function createPerson(firstName, lastName, height, weight, gender) {
  // function body
}
// call
const person = createPerson("Arya", "Stark", 4.6, "43kg", "female");
```

###### Use:

```javascript
function createPerson(parameter) {
  // extract arguments
  const { firstName, lastName, height, weight, gender } = parameter;

  // function body
}
//call
const person = createPerson({
  firstName: "Arya",
  lastName: "Stark",
  height: 4.6,
  weight: "43kg",
  gender: "female"
});
```

# Image Gallery

# Async API Data
