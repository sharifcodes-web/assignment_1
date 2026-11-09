# TypeScript Problem Solving & Blog Assignment

## Project Structure

- `solutions.ts` – All 8 problem solutions
- `type-vs-interface.md` – Blog 1
- `type-narrowing.md` – Blog 2
- `README.md` – Project documentation

## How to Run

First, compile the TypeScript file:

```bash
tsc solutions.ts
```

Then, run the generated JavaScript file:

```bash
node solutions.js
```

To check for TypeScript errors without generating a JavaScript file:

```bash
tsc solutions.ts --noEmit --target ES2020
```

## Concepts Covered

- Optional and default parameters
- Union types and type narrowing
- Readonly tuples
- Generics with `keyof` constraints
- Interfaces and array filtering
- OOP: classes, inheritance, and access modifiers
- Asynchronous programming with Promises

## Blog Posts

- [Type Aliases vs Interfaces](./type-vs-interface.md)
- [Type Narrowing in TypeScript](./type-narrowing.md)