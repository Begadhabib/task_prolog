

````markdown
# Shape Validator in Prolog

This Prolog project defines and validates 2D and 3D geometric shapes by checking specific conditions for each shape. It is ideal for learning logic programming and geometric reasoning using Prolog.

## 📁 Project Structure

- **Shape Definitions:** Supports various 1D, 2D, and 3D shapes.
- **Validation Rules:** Ensures input parameters for each shape meet required conditions.
- **Example Queries:** Demonstrates both valid and invalid cases for shape validation.

## ✅ Supported Shapes

### 1D Shapes
- `point(X, Y)`
- `line(X1, Y1, X2, Y2)`

### 2D Shapes
- `circle(Radius)`
- `square(Side)`
- `rectangle(Length, Width)`
- `triangle(A, B, C)`

### 3D Shapes
- `cube(Side)`
- `cuboid(Length, Width, Height)`
- `sphere(Radius)`
- `cylinder(Radius, Height)`

## 🔍 Predicate Overview

```prolog
valid_shape(Shape).
````

This is the main predicate used to check whether a shape is valid based on its parameters and geometry rules.

## 📌 Sample Valid Queries

```prolog
valid_shape(circle(5)).
valid_shape(square(4)).
valid_shape(point(1, 2)).
valid_shape(cylinder(3, 10)).
valid_shape(triangle(3, 4, 5)).
```

## ⚠️ Sample Invalid Queries

```prolog
valid_shape(circle(-2)).         % Negative radius
valid_shape(square(0)).          % Zero side length
valid_shape(rectangle(5, 5)).    % Length and width must not be equal
valid_shape(triangle(1, 2, 10)). % Violates triangle inequality
valid_shape(line(1, 1, 1, 1)).   % Zero-length line
```

## 🧠 Logic Highlights

* Triangle validation follows the **triangle inequality theorem**.
* Rectangle validation ensures **length ≠ width**, differentiating it from a square.
* Line validation checks **start and end points are not identical**.

## 🛠 Requirements

* SWI-Prolog or any other compatible Prolog interpreter.

## 🚀 Getting Started

1. Install [SWI-Prolog](https://www.swi-prolog.org/).
2. Load the Prolog file:

   ```bash
   swipl shapes.pl
   ```
3. Run sample queries:

   ```prolog
   valid_shape(circle(5)).
   ```

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).

---

Happy coding with logic! 🧮

