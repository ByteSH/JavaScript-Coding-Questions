# JavaScript Coding Questions
 
---
 
#### Click :star: if you like it!!
 
Every contribution counts, no matter how small. Join me on this exciting journey of open-source collaboration and learning. Together, let's build something amazing! 🚀
 
---
 
## 📘 Technical Concepts
 
**Prime number**: A whole number greater than 1 that has exactly two factors — 1 and itself. Example: 2, 3, 5, 7, 11... (2 is the only even prime number; every other even number has more than two factors, so it's not prime.)

**Whole numbers**: All the counting numbers together with zero. Example: 0, 1, 2, 3, 4, 5, 6...

**Factorial**: The result of multiplying a whole number by every whole number below it, all the way down to 1. e.g. 5! = 5x4x3x2x1 = 120

**Factor**: A whole number that divides into another number exactly, leaving no remainder. (e.g. 3 and 4 are factors of 12).

**Palindrome**: A number or word that reads the same backward as it does forward. Examples: 121, MADAM.

**Composite**: A positive integer greater than 1 that has more than two factors.

**Dividend**: The number being divided (inside the box/numerator). (e.g. 17/5 where dividend is 17)

**Divisor**: The number you are dividing by (outside the box/denominator). (e.g. 17/5 where Divisor is 5)

**Quotient**: Result of the division. (e.g. 17/5 where Quotient is 3)

**Remainder**: The amount left over that cannot be fully divided. (e.g. 17/5 where Remainder is 2)

**Union**: Combines all elements from two or more sets into one, removing duplicates. (e.g. A={1,2,3}, B={3,4,5}. Result={1,2,3,4,5})

**Intersection**: Identifies only the elements shared between sets. (e.g. A={1,2,3}, B={3,4,5}. Result={3})

**Recursion**: A programming technique where a function calls itself to solve a particular problem.
 
---
 
## 💻 Questions
 
**1. Find the element occurrence in the given array using a `for...of` loop**
 
```js
const arr = [1, 2, 3, 4, 5, 6, 7, 3, 4, 6, 3, 3, 4, 6, 3, 4];
const res = {};
 
for (const number of arr) {
    res[number] = (res[number] || 0) + 1;
}
 
console.log(res);
```

---
 
**2. Counting occurrences using `reduce`**
 
```js
const fruits = ['apple', 'banana', 'apple', 'orange', 'banana', 'apple'];
 
const fruitCount = fruits.reduce((counts, fruit) => {
    counts[fruit] = (counts[fruit] || 0) + 1;
    return counts;
}, {});
 
console.log(fruitCount);
```
