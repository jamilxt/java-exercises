# Iterating over the Elements of a Collection
## Using the for-each Pattern
Your simplest choice to iterate over the elements of a collection is to use the for-each pattern.  

```java
Collection<String> strings = List.of("one", "two", "three");

for (String element : strings) {
    System.out.println(element);
}
```
**Output:**  
```
one  
two  
three  
```

### Notes:  
- **For-each Loop**: The simplest way to iterate over a collection.  
- **Usage**: `for (ElementType element : collection) { }`  
- **Efficiency**: Works well when only reading elements.  
- **Limitation**: Cannot remove elements while iterating.  
- **Alternative**: Use the `Iterator` pattern if element removal is needed during iteration.

---

## Using an Iterator on a Collection
### Key Points:  
- **Iterator Interface**: Used to iterate over elements of a collection.  
- **Getting an Iterator**: Call `iterator()` on any `Collection` implementation.  
- **Iteration Process**:  
  1. Check if more elements exist using `hasNext()`.  
  2. Retrieve the next element using `next()`.  
- **Exception Handling**: Calling `next()` without checking `hasNext()` may result in `NoSuchElementException`.  
- **Example Usage**: Iterating over a list and printing elements with length 3.  
- **remove() Method**:  
  - Removes the current element from the collection.  
  - Throws `UnsupportedOperationException` if not supported (e.g., immutable collections).  
  - Supported by `ArrayList`, `LinkedList`, and `HashSet`.
