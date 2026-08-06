# Homework. Module 4. Arrays

## Overview

Complete each task in its corresponding JavaScript file:

- `task-1.js`
- `task-2.js`
- `task-3.js`

After implementing each solution, paste the provided test code below your function and leave it unchanged so your mentor can verify the results.

---

# Task 1. Slug Generator

Complete this task in **`task-1.js`**.

Before solving the task, let's introduce a new term.

A **slug** is a human-readable unique identifier commonly used in web development to create clean, readable URLs.

For example, instead of:

```text
mysite.com/posts/1q8fh74tx
```

you can generate a slug from the article title:

```text
mysite.com/posts/arrays-for-begginers
```

A slug is always:

- written in lowercase,
- with words separated by hyphens (`-`).

## Requirements

Write a function named `slugify(title)`.

The function accepts a string parameter `title` and returns a slug generated from it.

Assume that:

- words in `title` are separated only by spaces;
- all characters in the slug must be lowercase;
- words in the slug must be separated with hyphens.

### Test your solution

```javascript
console.log(slugify("Arrays for begginers"));
// "arrays-for-begginers"

console.log(slugify("English for developer"));
// "english-for-developer"

console.log(slugify("Ten secrets of JavaScript"));
// "ten-secrets-of-javascript"

console.log(slugify("How to become a JUNIOR developer in TWO WEEKS"));
// "how-to-become-a-junior-developer-in-two-weeks"
```

> **Do not remove these test cases.** Leave them in your solution for your mentor to review.

## Review Checklist

- [x] - The `slugify(title)` function is declared.
- [x] - `slugify("Arrays for begginers")` returns `"arrays-for-begginers"`.
- [x] - `slugify("English for developer")` returns `"english-for-developer"`.
- [x] - `slugify("Ten secrets of JavaScript")` returns `"ten-secrets-of-javascript"`.
- [x] - `slugify("How to become a JUNIOR developer in TWO WEEKS")` returns `"how-to-become-a-junior-developer-in-two-weeks"`.

---

# Task 2. Array Composition

Complete this task in **`task-2.js`**.

## Requirements

Write a function named `makeArray(firstArray, secondArray, maxLength)`.

The function accepts three parameters:

- `firstArray` — the first array.
- `secondArray` — the second array.
- `maxLength` — the maximum allowed length of the resulting array.

The function should:

1. Create a new array containing all elements from `firstArray`, followed by all elements from `secondArray`.
2. If the resulting array contains more than `maxLength` elements, return a copy containing only the first `maxLength` elements.
3. Otherwise, return the entire array.

### Test your solution

```javascript
console.log(makeArray(["Mango", "Poly"], ["Ajax", "Chelsea"], 3));
// ["Mango", "Poly", "Ajax"]

console.log(makeArray(["Mango", "Poly", "Houston"], ["Ajax", "Chelsea"], 4));
// ["Mango", "Poly", "Houston", "Ajax"]

console.log(makeArray(["Mango"], ["Ajax", "Chelsea", "Poly", "Houston"], 3));
// ["Mango", "Ajax", "Chelsea"]

console.log(makeArray(["Earth", "Jupiter"], ["Neptune", "Uranus"], 2));
// ["Earth", "Jupiter"]

console.log(makeArray(["Earth", "Jupiter"], ["Neptune", "Uranus"], 4));
// ["Earth", "Jupiter", "Neptune", "Uranus"]

console.log(makeArray(["Earth", "Jupiter"], ["Neptune", "Uranus", "Venus"], 0));
// []
```

> **Do not remove these test cases.** Leave them in your solution for your mentor to review.

## Review Checklist

- [x] - The `makeArray(firstArray, secondArray, maxLength)` function is declared.
- [x] - `makeArray(["Mango", "Poly"], ["Ajax", "Chelsea"], 3)` returns `["Mango", "Poly", "Ajax"]`.
- [x] - `makeArray(["Mango", "Poly", "Houston"], ["Ajax", "Chelsea"], 4)` returns `["Mango", "Poly", "Houston", "Ajax"]`.
- [x] - `makeArray(["Mango"], ["Ajax", "Chelsea", "Poly", "Houston"], 3)` returns `["Mango", "Ajax", "Chelsea"]`.
- [x] - `makeArray(["Earth", "Jupiter"], ["Neptune", "Uranus"], 2)` returns `["Earth", "Jupiter"]`.
- [x] - `makeArray(["Earth", "Jupiter"], ["Neptune", "Uranus"], 4)` returns `["Earth", "Jupiter", "Neptune", "Uranus"]`.
- [x] - `makeArray(["Earth", "Jupiter"], ["Neptune", "Uranus", "Venus"], 0)` returns `[]`.
- [x] - The function returns the correct array for any valid input.

---

# Task 3. Filter an Array of Numbers

Complete this task in **`task-3.js`**.

## Requirements

Write a function named `filterArray(numbers, value)`.

The function accepts:

- `numbers` — an array of numbers.
- `value` — a number used as the filtering threshold.

The function should return a new array containing only the numbers that are **greater than** `value`.

Inside the function:

1. Create an empty array to store matching values.
2. Use a loop to iterate through every element of `numbers`.
3. Use an `if` statement to check each value and add it to the new array when appropriate.
4. Return the new array.

### Test your solution

```javascript
console.log(filterArray([1, 2, 3, 4, 5], 3));
// [4, 5]

console.log(filterArray([1, 2, 3, 4, 5], 4));
// [5]

console.log(filterArray([1, 2, 3, 4, 5], 5));
// []

console.log(filterArray([12, 24, 8, 41, 76], 38));
// [41, 76]

console.log(filterArray([12, 24, 8, 41, 76], 20));
// [24, 41, 76]
```

> **Do not remove these test cases.** Leave them in your solution for your mentor to review.

## Review Checklist

- [x] - The `filterArray(numbers, value)` function is declared.
- [x] - `filterArray([1, 2, 3, 4, 5], 3)` returns `[4, 5]`.
- [x] - `filterArray([1, 2, 3, 4, 5], 4)` returns `[5]`.
- [x] - `filterArray([1, 2, 3, 4, 5], 5)` returns `[]`.
- [x] - `filterArray([12, 24, 8, 41, 76], 38)` returns `[41, 76]`.
- [x] - `filterArray([12, 24, 8, 41, 76], 20)` returns `[24, 41, 76]`.
- [x] - The function returns the correct array for any valid input.
