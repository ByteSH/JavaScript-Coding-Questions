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
 
**1. Find the element occurrence in the given array using a loop**
 
```js
const arr = [1, 2, 3, 4, 5, 6, 7, 3, 4, 6, 3, 3, 4, 6, 3, 4];
const res = {};
 
for (const number of arr) {
    res[number] = (res[number] || 0) + 1;
}
 
console.log(res);
```

---
 
**2. Counting elements of array occurrences using `reduce`**
 
```js
const fruits = ['apple', 'banana', 'apple', 'orange', 'banana', 'apple'];
 
const fruitCount = fruits.reduce((counts, fruit) => {
    counts[fruit] = (counts[fruit] || 0) + 1;
    return counts;
}, {});
 
console.log(fruitCount);
```

---

**3. Create #Tag from a sentence**
 
```js
let str = "We are dev, human";
 
console.log("#", str.replace(/[,.]/g, "").split(" ").map(w => w[0].toUpperCase() + w.slice(1)).join(""));
```
  
---
 
**4. Loop basics — `for...in`, `for...of`, `forEach`**
 
```js
const person = { name: "Hamza", city: "Mumbai" };
 
for (let key in person) {
    console.log(key + ": " + person[key]);
}
 
const colors = ["Red", "Green"];
 
for (let color of colors) {
    console.log(color);
}
 
const numbers = [10, 20];
 
numbers.forEach((num, index) => {
    console.log(`Index ${index} par value hai: ${num}`);
});
 
let str = "Hamza";
 
for (let char of str) {
    console.log(char);
}
 
let num = 1234567;
let digits = Array.from(String(num), Number);
 
digits.forEach(d => console.log(d));
```
  
---
 
**5. Important Array functions.**
add element at end,at start.
remove elements from start, from end.
create new array having elements from 0 to 2.
find elements included.
find index of element.
ascending and descending sorting.
use map, filter, reduce, find, forEach with index and element.
 
```js
let products = ["Laptop", "Mouse", "Keyboard", "Monitor"];
 
products.push("Headphones");
products.unshift("Webcam");
products.pop();
products.shift();
 
let topTwo = products.slice(0, 2);
console.log("Top 2 Products:", topTwo);
 
console.log(products.includes("Mouse"));
console.log(products.indexOf("Speaker"));
 
products.sort();
products.reverse();
 
const prices = [50000, 1500, 8000, 12000];
const pricesWithGST = prices.map(p => p + (p * 0.18));
const affordable = pricesWithGST.filter(p => p < 10000);
const totalBill = pricesWithGST.reduce((total, p) => total + p, 0);
 
const costlyPrice = pricesWithGST.find(p => p > 20000);
 
const productListString = products.join(" | ");
console.log("Catalog:", productListString);
 
products.forEach((item, index) => {
    console.log(`Product ${index + 1}: ${item}`);
});
```
  
---
 
**6. String and Number sorting in objects**
 
```js
const items = [
    {name: "Laptop", price: 50000},
    {name: "Mouse", price: 1500},
    {name: "Keyboard", price: 2500}
];
 
items.sort((a, b) => a.price - b.price);
 
items.sort((a, b) => a.name.localeCompare(b.name));
```
  
---
 
**7. Find the longest word from the string**
 
```js
let str = "Hi team hamza this side";
 
console.log(
    str.split(" ").sort((a, b) => b.length - a.length).at(0)
);
```
  
---
 
**8. Find missing number from a sequential array**
 
```js
let arr = [1, 2, 3, 5, 6, 7, 9, 10];
let position = 0;
 
for (let i = Math.min(...arr); i < Math.max(...arr); i++) {
    if (arr[position] === i) {
        position++;
    } else {
        console.log(i);
    }
}
```
  
---
 
**9. Reverse a String**
 
```js
let str = "hamza this side";
 
console.log(
    str.split("").reverse().join("")
);
```
  
---
 
**10. Star Pattern**
 
```js
let n = 5;
 
for (let i = 1; i <= n; i++) {
    let row = "";
    for (let j = 1; j <= i; j++) {
        row += "* ";
    }
    console.log(row);
}
 
console.log('====================================================');
 
const rows = 4;
 
for (let i = 0; i < rows; i++) {
    const gap = "  ".repeat(i);
    const stars = "* ".repeat(8 - i * 2);
    console.log(gap + stars);
}
```
  
---
 
**11. Check if a character is UpperCase, LowerCase, or a Number**
 
```js
function isUpperCase(char) {
    const code = char.charCodeAt(0);
    return code >= 65 && code <= 90;
}
 
function isLowerCase(char) {
    const code = char.charCodeAt(0);
    return code >= 97 && code <= 122;
}
 
function isNumber(char) {
    const code = char.charCodeAt(0);
    return code >= 48 && code <= 57;
}
 
const char1 = 'A';
const char2 = 'b';
const char3 = '7';
 
console.log(`"${char1}" is uppercase: ${isUpperCase(char1)}`);
console.log(`"${char2}" is lowercase: ${isLowerCase(char2)}`);
console.log(`"${char3}" is a number: ${isNumber(char3)}`);
```
    
---
 
**12. Recursion — Find Factorial of a number**
 
```js
const factorial = (n) => {
    if (n === 0 || n === 1) {
        return 1;
    }
    return n * factorial(n - 1);
}
 
console.log(
    factorial(5)
);
```
  
---
 
**13. Fibonacci number**
 
```js
function getFibonacci(n) {
    let fib = [0, 1];
 
    for (let i = 2; i < n; i++) {
        fib[i] = fib[i - 1] + fib[i - 2];
    }
 
    return fib;
}
 
console.log(getFibonacci(10));
```
  
---
 
**14. Palindrome, Anagram & Armstrong Number**
 
```js
function isPalindrome(str) {
    return str === str.split('').reverse().join('');
}
 
function isAnagram(str1, str2) {
    const format = (s) => s.toLowerCase().split('').sort().join('');
    return format(str1) === format(str2);
}

function findArmstrong(num) {
    const digits = String(num).split("").map(Number);
    const power = digits.length;
    let sum = digits.reduce((acc, digit) => acc + Math.pow(digit, power), 0);
    return sum === num;
}


let text = "madam";
console.log(isPalindrome(text));

let word1 = "listen";
let word2 = "silent";
console.log(isAnagram(word1, word2));

let number = 153;
console.log(findArmstrong(number));
```
  
---
 
**15. Find min difference between 2 array elements**
 
```js
let arr = [1, -2, 4, -5, 6, -7, 10];
 
function minDiffCorrected(arr) {
    if (arr.length < 2) return 0;
 
    arr.sort((a, b) => a - b);
 
    let diff = Infinity;
 
    for (let i = 0; i < arr.length - 1; i++) {
        let currentDiff = arr[i + 1] - arr[i];
 
        if (currentDiff < diff) {
            diff = currentDiff;
        }
    }
    return diff;
}
 
console.log(minDiffCorrected(arr));
```
  
---
 
**16. Prime Number**
 
```js
function isPrime(num) {
    if (num <= 1) return false;
    if (num === 2) return true;
    if (num % 2 === 0) return false;
 
    for (let i = 3; i <= Math.sqrt(num); i += 2) {
        if (num % i === 0) {
            return false;
        }
    }
    return true;
}
 
console.log(isPrime(29));
console.log(isPrime(15));
```
  
---
 
**17. Composite Numbers**
 
```js
function isComposite(num) {
    if (num <= 1) return false;
 
    for (let i = 2; i <= Math.sqrt(num); i++) {
        if (num % i === 0) {
            return true;
        }
    }
 
    return false;
}
 
console.log(isComposite(4));
console.log(isComposite(9));
console.log(isComposite(7));
console.log(isComposite(1));
```
  
---
 
**18. Dividend, Divisor, Quotient & Remainder**
 
```js
let dividend = 17;
let divisor = 5;
 
let remainder = dividend % divisor;
 
let quotient = Math.floor(dividend / divisor);
 
console.log("Quotient:", quotient);
console.log("Remainder:", remainder);
```
  
---
 
**19. Union & Intersection**
 
```js
let arrA = ["Apple", "Banana", "Mango"];
let arrB = ["Mango", "Orange", "Watermelon"];
 
let union = [...new Set([...arrA, ...arrB])];
 
console.log(union);
 
let intersection = arrA.filter(element => arrB.includes(element));
 
console.log(intersection);
```
