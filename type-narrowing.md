Type Narrowing in TypeScript

Introduction

Type Narrowing is an important feature in TypeScript that allows developers to convert a broad type into a more specific type within a conditional block. It helps TypeScript understand which type of value is being used at a particular point in the code. As a result, developers can safely access properties and methods without using any.

Body

One common technique is the typeof operator, which checks primitive types such as strings and numbers.

function format(value: string | number): string {
if (typeof value === "string") {
return value.toUpperCase();
}
return value.toFixed(2);
}

Here, TypeScript understands that value is a string inside the first block and a number after the condition.

The instanceof operator checks whether an object belongs to a particular class.

class Dog {
bark(): string {
return "Woof";
}
}

class Cat {
meow(): string {
return "Meow";
}
}

function speak(animal: Dog | Cat): string {
if (animal instanceof Dog) {
return animal.bark();
}
return animal.meow();
}

The in operator checks whether an object contains a specific property.

type Admin = { role: "admin"; permissions: string[] };
type Guest = { role: "guest" };

function describe(user: Admin | Guest): string {
if ("permissions" in user) {
return `Admin with ${user.permissions.length} permissions`;
}
return "Guest user";
}

TypeScript also supports truthiness checks, equality checks, and custom type guards to narrow types further.

Conclusion

Type Narrowing makes TypeScript code safer, clearer, and easier to maintain. By using typeof, instanceof, and the in operator, developers can handle union types effectively without sacrificing type safety or relying on any.
