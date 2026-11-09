# Generics in TypeScript and Their Role in Asynchronous Promise Responses

## Introduction

Generics are an important feature of TypeScript that help developers write reusable and type-safe code. They allow functions, classes, and interfaces to work with different data types without losing type information. Generics are especially useful when handling asynchronous operations with `Promise<T>`.

## 1. Understanding Generics

Generics allow us to create a single function that works with different data types instead of writing separate functions for each type. We commonly use `<T>` as a placeholder for a data type.

Example :
function getValue<T>(value: T): T {
  return value;
}

getValue<number>(100);
getValue<string>("Abir");

Here, `T` represents the input data type, and the function returns the same type it receives. This makes the function reusable while maintaining type safety.

## 2. Understanding Promise<T>

A Promise represents the eventual result of an asynchronous operation, such as fetching data from an API. In TypeScript, `Promise<T>` specifies the type of value returned when the Promise is successfully resolved.

Example :
async function getUser(): Promise<string> {
  return "Abir";
}

Here, `Promise<string>` means the function returns a Promise that resolves with a string.

## 3. Combining Generics with Promise<T>

Generics make asynchronous functions more flexible because one function can handle different response types.

Example :
async function fetchData<T>(data: T): Promise<T> {
  return data;
}

const result = await fetchData<number>(100);

Here, the function accepts different data types and returns a Promise containing the same type.

## Conclusion

In conclusion, Generics help developers create reusable and type-safe code, while `Promise<T>` ensures type safety for asynchronous results. Combining them makes applications easier to maintain, especially when working with APIs and backend development.