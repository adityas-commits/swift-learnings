## Tuples

A tuple is a compound type in Swift that groups multiple related values into a single value, and those values can be of different data types. Tuple elements are accessed by index or by name (if named). If declared with var, you can modify existing elements (while keeping their types the same), but you cannot add, remove, or change the types of elements.

---

## Optionals

| Concept | Syntax | Meaning |
|---------|--------|---------|
| Non-Optional | `String` | Must always have a value. Cannot be `nil`. |
| Optional | `String?` | Can contain a value or `nil`. |
| `nil` | `var name: String? = nil` | Represents the absence of a value. |
| Force Unwrapping | `name!` | Extracts the value. Crashes if `nil`. |
| Optional Binding | `if let name = name {}` | Safely unwraps the optional. |
| Guard Binding | `guard let name = name else { return }` | Safely unwraps and exits early if `nil`. |
| Optional Chaining | `name?.count` | Accesses a property/method only if the optional has a value. Returns an optional. |
| Nil Coalescing | `name ?? "Guest"` | Returns the value if present; otherwise returns the default value. |
