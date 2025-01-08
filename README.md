# Kotlin ConcurrentModificationException Example

This repository demonstrates a common error in Kotlin involving `ConcurrentModificationException` when modifying a collection (like `List` or `Map`) while iterating over it using a traditional `for` loop. The safe way to achieve the same result is also provided.

## Problem

Directly modifying a collection (adding or removing elements) within a `for` loop iteration throws a `ConcurrentModificationException`. This is because the iterator used by the `for` loop becomes invalidated when the underlying collection is structurally modified.

## Solution

The preferred approach is to use the collection's built-in methods like `removeIf` which are designed for safe modification during iteration. Alternatively, use an iterator and its `remove()` method, which will perform the removal in a thread safe manner.