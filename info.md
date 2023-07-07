## Basic Data Structures: Introduction

Data structures are fundamental to programming and can be thought of as collections of data in a specific organization or structure. This allows efficient access and modification of the data. Different types of data structures include Arrays, Objects, Sets, and Maps, which are commonly used in web development.

## Sets

A Set is a special type of data structure provided by ES6 (ECMAScript 2015) in JavaScript. A Set is a collection of unique values. Any type of value can be added to a Set: objects, primitive values, or both.

Creating a Set in JavaScript:
```javascript
let mySet = new Set();
```
Adding values to a Set:
```javascript
mySet.add(1); // Set { 1 }
mySet.add(2); // Set { 1, 2 }
mySet.add(1); // Set { 1, 2 } - no change, as 1 is already in the set
```

## Maps

A Map is a data structure that pairs keys with values. Like Sets, Maps were also introduced in ES6. A Map allows keys of any type and maintains the insertion order.

Creating a Map in JavaScript:
```javascript
let myMap = new Map();
```
Adding values to a Map:
```javascript
myMap.set('name', 'Alice'); // Map { 'name' => 'Alice' }
myMap.set('age', 30); // Map { 'name' => 'Alice', 'age' => 30 }
```

## Arrays

An Array is a linear data structure consisting of a collection of elements, identified by integer index. Arrays are one of the simplest and most commonly used data structures.

Creating an Array in JavaScript:
```javascript
let myArray = [];
```
Adding values to an Array:
```javascript
myArray.push(1); // [1]
myArray.push(2); // [1, 2]
```

## Objects

An Object in JavaScript is an unordered collection of key-value pairs. If a map is a more general form of an array, then an object is a more general form of a map.

Creating an Object in JavaScript:
```javascript
let myObject = {};
```
Adding values to an Object:
```javascript
myObject['name'] = 'Alice'; // { 'name': 'Alice' }
myObject['age'] = 30; // { 'name': 'Alice', 'age': 30 }
```

## Filtering Data Structures: Arrays

Filtering is a method provided by the array to check each element of the array and return a new array that fulfills the condition provided for the filter.

Filtering in an Array:
```javascript
let numbers = [1, 2, 3, 4, 5];
let evenNumbers = numbers.filter(number => number % 2 === 0);
console.log(evenNumbers); // [2, 4]
```

## Filtering Data Structures: Objects

Filtering objects can be achieved by turning the objects into an array, applying filter, then turning it back into an object.

Filtering in an Object:
```javascript
let student = {
  name: 'Alice',
  age: 20,
  grade: 'A',
};

let filteredStudent = Object.keys(student)
.filter(key => key !== 'age')
.reduce((obj, key) => {
  obj[key] = student[key];
  return obj;
}, {});

console.log(filteredStudent); // { name: 'Alice', grade: 'A' }
```

## Filtering Data Structures: Sets

Filtering in Sets involves converting the Set into an Array, applying the filter, and converting it back to a Set if necessary.

Filtering in a Set:
```javascript
let mySet = new Set([1, 2, 3, 4, 5]);
mySet = new Set([...mySet].filter(x => x%2 === 0));
console.log(mySet); // Set {2, 4}
```

## Filtering Data Structures: Maps

Filtering Maps is similar to Sets - convert the Map into an Array, apply the filter, then convert back to a Map.

Filtering in a Map:
```javascript
let studentMap = new Map();
studentMap.set('name', 'Alice');
studentMap.set('age', 20);
studentMap.set('grade', 'A');

let filteredMap = new Map([...studentMap].filter(([k, v]) => k !== 'age'));
console.log(filteredMap); // Map { 'name' => 'Alice', 'grade' => 'A' }
```

## A Primer on Big O Notation

Big O notation is used in computer science to describe the performance or complexity of an algorithm. Big O specifically describes the worst-case scenario, or the maximum amount of time taken by an algorithm. Here are a few examples:

1. O(1): Constant time complexity. No matter how much data, the operation takes the same amount of time.
2. O(n): Linear time complexity. The time taken grows linearly with the size of the data.
3. O(n^2): Quadratic time complexity. Time taken grows quadratically with the size of the data.

Understanding Big O notation and time complexity is essential for writing efficient code, particularly in applications dealing with large amounts of data.
![Big O Notation Summary](https://images.squarespace-cdn.com/content/v1/51e97622e4b001fd0a6bba71/1521928168525-QM8F87Q76TVYKLO33A0N/Big%2BO%2BNotation%2BSummary.jpg?format=750w)
![Time complexity of an algorithm](https://media.licdn.com/dms/image/C5112AQELJi9rrpPeTw/article-cover_image-shrink_423_752/0/1520133128080?e=1694044800&v=beta&t=bVa3gU7qBgdJz-mCyMxPN92SWhqfmwi1L3C4YjtNjuw)
