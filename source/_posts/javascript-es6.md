---
title: JavaScript ES6+ 常用特性总结
date: 2026-04-22 10:00:00
tags:
  - JavaScript
  - ES6
  - 前端
categories:
  - 技术笔记
---

ES6（ECMAScript 2015）及其后续版本为 JavaScript 带来了许多强大的新特性。本文总结了我在日常开发中最常用的 ES6+ 特性。

## 1. 箭头函数

箭头函数提供了一种更简洁的函数定义方式，同时解决了 `this` 指向的问题。

```javascript
// 传统函数
function add(a, b) {
  return a + b;
}

// 箭头函数
const add = (a, b) => a + b;

// 带函数体
const multiply = (a, b) => {
  const result = a * b;
  return result;
};
```

## 2. 解构赋值

从数组或对象中提取值，赋值给变量。

```javascript
// 数组解构
const [first, second, ...rest] = [1, 2, 3, 4, 5];
// first = 1, second = 2, rest = [3, 4, 5]

// 对象解构
const { name, age } = { name: 'Alice', age: 25 };

// 函数参数解构
function greet({ name, age }) {
  return `Hello, I'm ${name}, ${age} years old.`;
}
```

## 3. 模板字符串

使用反引号 `` ` `` 定义字符串，支持嵌入变量和表达式。

```javascript
const name = 'World';
const message = `Hello, ${name}!`;

// 多行字符串
const html = `
<div class="card">
  <h2>${title}</h2>
  <p>${content}</p>
</div>
`;
```

## 4. Promise 和 async/await

处理异步操作。

```javascript
// Promise
fetch('/api/data')
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error(error));

// async/await
async function fetchData() {
  try {
    const response = await fetch('/api/data');
    const data = await response.json();
    return data;
  } catch (error) {
    console.error(error);
  }
}
```

## 5. 展开运算符

```javascript
// 数组展开
const arr1 = [1, 2, 3];
const arr2 = [...arr1, 4, 5]; // [1, 2, 3, 4, 5]

// 对象展开
const obj1 = { a: 1, b: 2 };
const obj2 = { ...obj1, c: 3 }; // { a: 1, b: 2, c: 3 }
```

## 6. 可选链和空值合并

```javascript
// 可选链
const user = {
  profile: {
    name: 'Alice'
  }
};
const city = user?.profile?.city; // undefined

// 空值合并
const value = null ?? 'default'; // 'default'
```

---

掌握这些 ES6+ 特性可以让你的 JavaScript 代码更加简洁和优雅。建议在日常开发中多加练习，逐渐掌握这些特性。