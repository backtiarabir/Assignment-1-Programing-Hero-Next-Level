# Type vs Interface in TypeScript: Understanding the Differences and When to Use Them

## Introduction

When working with TypeScript, we often need to define the structure of our data. For this purpose, TypeScript provides two useful features: `type` aliases and `interface`. Both help us organize our code and maintain type safety. Although they look similar and can do many of the same things, there are some differences between them. Understanding these differences helps us decide which one to use in different situations.

## 1. What is an Interface?

An `interface` is used to describe the structure of an object. It tells us what properties and methods an object should have and what types they should follow.

For example:

```typescript
interface Student {
  name: string;
  age: number;
  department: string;
}

const student: Student = {
  name: "Abir",
  age: 25,
  department: "CSE"
};
```

Here, the `Student` interface defines three properties. Any object using this interface must follow the same structure. If a required property is missing or has the wrong type, TypeScript will show an error.

## 2. What is a Type Alias?

A `type` alias allows us to give a custom name to a type. It can be used for objects, primitive values, unions, tuples, and function types.

```typescript  Example:
type Student = {
  name: string;
  age: number;
  department: string;
};

const student: Student = {
  name: "Abir",
  age: 25,
  department: "CSE"
};
```
We can also create other type using type alias.

```typescript Example:
type UserId = number;
type Status = "pending" | "success" | "failed";
type Coordinate = [number, number];
```

## 3. Key Differences

One important difference is declaration merging. An interface can be declared multiple times with the same name, and TypeScript automatically combines them. However, type aliases do not support declaration merging.

Another difference is how they extend existing structures. Interfaces use the `extends` keyword, while type aliases use the intersection (`&`) operator to combine types.

```typescript Example:
interface Person {
  name: string;
}

interface Employee extends Person {
  salary: number;
}
```

The same structure can be created using a type alias:

```typescript Example: 
type Person = {
  name: string;
};

type Employee = Person & {
  salary: number;
};
```

## 4. Advantages and Disadvantages

**Interface:**
- Supports declaration merging.
- Makes object structures easier to extend.
- Works well with classes and object-oriented programming.

**Type Alias:**
- Supports union and intersection types.
- Can represent primitive types, tuples, and functions.
- Offers more flexibility when creating complex types.

In general, I would choose an interface when defining object structures and a type alias when working with unions, tuples, or more complex type combinations.

## Conclusion

Both `type` and `interface` are useful features in TypeScript. They have many similarities, but each has its own strengths. The best choice depends on what we are trying to build and how we want to organize our code.