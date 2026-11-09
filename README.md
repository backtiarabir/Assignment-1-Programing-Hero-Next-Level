# Assignment-1-Programing-Hero-Next-Level
# TypeScript Core Concepts & Problem Solving

Welcome to this repository! This project contains a collection of clean, practical solutions demonstrating core TypeScript features—ranging from basic type narrowing and tuples to advanced generics, object-oriented programming (OOP), and asynchronous operations.

Instead of just making the code work, the goal here was to write readable, strictly-typed, and predictable TypeScript.

## What's Inside?

Here is a quick breakdown of the 8 problems solved in this project and the TypeScript concepts behind them:

### 1. Optional Parameters (`multiplyValue`)
Handles optional inputs gracefully. If a custom multiplier is provided, it multiplies the value by that number; otherwise, it falls back to doubling the value (`* 2`).
- **Concepts used:** Optional parameters (`?`), strict `undefined` checking.

### 2. Union Types & Type Narrowing (`processInput`)
A flexible utility function that accepts a `string`, `number`, or `boolean` and processes it differently based on its runtime type:
- **Strings** are trimmed and converted to lowercase.
- **Numbers** are multiplied by 10.
- **Booleans** return a readable status (`"Active"` or `"Inactive"`).
- **Concepts used:** Union types (`|`), `typeof` type guards.

### 3. Readonly Tuples & Destructuring (`formatCoordinate`)
Takes a fixed structure of geographical data—latitude, longitude, and a location name—and formats it into a clean, readable string.
- **Concepts used:** `readonly` tuples, parameter destructuring, template literals.

### 4. Generic Array Flattening (`concatenateArrays`)
Merges multiple arrays of the same type into a single flat array without losing type safety, regardless of how many arrays are passed in.
- **Concepts used:** Generics (`<T>`), rest parameters (`...`), `Array.prototype.reduce`.

### 5. Interfaces & Data Filtering (`getPopularCourses`)
Filters a list of courses to find the ones that are both published and meet a minimum student enrollment threshold.
- **Concepts used:** `interface` definitions, typed array methods (`filter`).

### 6. Type-Safe Property Extraction (`pluckValues`)
Extracts a specific property from an array of objects. Using `keyof`, TypeScript ensures at compile-time that you can only ask for properties that actually exist on the object.
- **Concepts used:** Bounded generics (`K extends keyof T`), indexed access types (`T[K]`).

### 7. Object-Oriented Programming (`Employee` & `Manager`)
Models a simple company hierarchy where `Manager` inherits from `Employee`, demonstrating how access modifiers control data visibility across classes.
- **Concepts used:** Classes, inheritance (`extends`), `super()`, and access modifiers (`private` vs `protected`).

### 8. Asynchronous Validation (`validateAgeAsync`)
Simulates an asynchronous age-verification check using Promises. It resolves after 1 second if the user is 18 or older, or immediately rejects with a descriptive `Error` if underage.
- **Concepts used:** `async/await`, `Promise<string>`, asynchronous error handling.

---

## Getting Started

If you want to run or test these functions locally on your machine, follow these steps:

### Prerequisites
Make sure you have [Node.js](https://nodejs.org/) installed, along with `typescript` and `ts-node` for quick execution.

