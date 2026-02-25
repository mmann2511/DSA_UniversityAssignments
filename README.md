# DSA Selector

Two implementations of a `Selector` utility class built as part of a Data Structures & Algorithms course at Auburn University. Both implementations provide the same core selection operations — the key difference is the underlying data type each works with.

---

## Projects

### 📁 `array-selector`
Implements selection operations on **primitive `int` arrays**. Methods are static and operate directly on `int[]` inputs.

### 📁 `collection-selector`
A generic, polymorphic implementation that operates on any **`Collection<T>`** using a `Comparator<T>` to define ordering. Works with any comparable object type.

---

## Methods

Both implementations provide the following operations:

| Method | Description |
|---|---|
| `min` | Returns the minimum value |
| `max` | Returns the maximum value |
| `kmin(k)` | Returns the k-th smallest distinct value |
| `kmax(k)` | Returns the k-th largest distinct value |
| `range(low, high)` | Returns all values within `[low, high]` |
| `floor(key)` | Returns the largest value ≤ key |
| `ceiling(key)` | Returns the smallest value ≥ key |

---

## Example Usage

### Array Selector
```java
int[] a = {2, 8, 7, 3, 4};
Selector.min(a);        // 2
Selector.kmin(a, 2);    // 3
Selector.floor(a, 6);   // 4
Selector.ceiling(a, 5); // 7
```

### Collection Selector
```java
List<Integer> list = Arrays.asList(2, 8, 7, 3, 4);
Comparator<Integer> comp = Comparator.naturalOrder();
Selector.min(list, comp);        // 2
Selector.kmin(list, 2, comp);    // 3
Selector.floor(list, 6, comp);   // 4
Selector.ceiling(list, 5, comp); // 7
```

---

## Tech Stack
- Java
- `java.util.Arrays` (array-selector)
- `java.util.Collections`, `java.util.Comparator` (collection-selector)

---

## Course
**COMP 2210 – Data Structures and Algorithms**  
Auburn University
