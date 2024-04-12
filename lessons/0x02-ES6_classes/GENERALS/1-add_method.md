Adding methods to a class in JavaScript is straightforward. You define methods within the class body using regular function syntax. These methods can then be invoked on instances of the class. Here's how to add methods to a class:

### 1. Instance Methods:

Instance methods are functions that are accessible on each instance of the class. They are defined without the `static` keyword within the class body.

```javascript
class MyClass {
  // Constructor
  constructor(param) {
    this.param = param;
  }

  // Instance method
  myMethod() {
    // Method logic
    return this.param;
  }
}
```

In this example, `myMethod` is an instance method that returns the value of the `param` property for the instance.

### 2. Static Methods:

Static methods are functions that are associated with the class itself, rather than with instances of the class. They are defined using the `static` keyword within the class body.

```javascript
class MyClass {
  // Static method
  static myStaticMethod() {
    // Static method logic
    return 'This is a static method';
  }
}
```

In this example, `myStaticMethod` is a static method that returns a string.

### Example:

```javascript
class Circle {
  constructor(radius) {
    this.radius = radius;
  }

  // Instance method to calculate area
  calculateArea() {
    return Math.PI * this.radius ** 2;
  }

  // Static method to return the circumference of a circle
  static calculateCircumference(radius) {
    return 2 * Math.PI * radius;
  }
}

// Create an instance of Circle
const myCircle = new Circle(5);

// Call instance method to calculate area
console.log(myCircle.calculateArea()); // Output: 78.53981633974483

// Call static method to calculate circumference
console.log(Circle.calculateCircumference(5)); // Output: 31.41592653589793
```

In this example, `calculateArea` is an instance method that calculates the area of a circle, while `calculateCircumference` is a static method that calculates the circumference of a circle.