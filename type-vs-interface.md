# Understanding Type Aliases vs. Interfaces

When we code in typeScript, their are two way to define types: Type Alias and Interface. Both are to define type but they have some diffrences.

## What is an Interface?

An Interface is generally designed for shape objects structure. We can't define literals, unions using Interface. Interface support inheritence using `extends` keyword. And also when we declare Interfaces with same name it merge them automatically.

## What is a Type Alias?

On the Other hand a type Alias is designed to give a custom name to any types. it's more connected to define literals, unions, tuples and primitive types. while Interface is strictly used for Object shape.

## Code Example

### Using Interface for an object shape

```
interface User {
name: string;
age: number;
}
```

### Using Type Alias for a union type

```
type role = "user" | "admin";
```

## Conclusion

As a general rule use `interface` for when defining Object structure. and Use `type` when working with literals, unions, tuples and primitive types. Both are powerful on their way.
