# Understanding Access Modifiers in TypeScript

In TypeScript access modifiers are used to set visibility of properties and methods. It protects data and help to write clean and secure code.

## The Four Modifiers

1. `public`: This is set by default. public properties and methods can be accessed from anywhere - inside, outside or sub classes.
2. `private`: This is strictly restricted. This only can accessible within the class. Even subclass can't access it.
3. `protected` This is similar to `private`. But It is accessible from sub classes. Still remain inaccessable from outside the class.
4. `readonly` Readonly properties allow set values only once. its value can be read but can't re-assign later.

## Code Example

```
class UserAccount {
  readonly userId: string; // Read-only: cannot be modified after creation
  public email: string; // Public: accessible from anywhere
  protected role: string; // Protected: accessible in this class and subclasses
  private password: string; // Private: strictly internal to this class

  constructor(userId: string, email: string, role: string, password: string) {
    this.userId = userId;
    this.email = email;
    this.role = role;
    this.password = password;
  }
}

// Subclass demonstrating 'protected' access
class AdminAccount extends UserAccount {
  constructor(userId: string, email: string, password: string) {
    super(userId, email, "Administrator", password);
  }

  getRole(): string {
    return this.role; // Accessible because 'role' is protected
  }
}
```

## Conclusion

Access modifier are essential for data safety in TypeScript. It prevent accedental data leaks and keep classes organized.
