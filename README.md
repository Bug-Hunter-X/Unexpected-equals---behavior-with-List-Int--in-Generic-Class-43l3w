# Scala Generic Class and List[Int] Comparison Issue

This repository demonstrates a subtle bug related to the comparison of `List[Int]` objects within a generic class in Scala. The `equals()` method doesn't behave as expected when comparing two `List[Int]` instances.

## Problem Description
The `MyClass` class is designed to hold a value of type `T`. The `myMethod` compares the `value` fields of two `MyClass` instances. While the comparison works correctly for primitive types like `Int` and `String`, it unexpectedly returns `false` when comparing `List[Int]` objects that contain the same elements.

## Steps to Reproduce
1. Run the `Main` object in the `MyClass.scala` file.
2. Observe the output. The comparison of `List[Int]` objects will unexpectedly return `false`. 

## Solution
The issue stems from the default `equals()` method provided by Scala's `List` class.  The solution involves overriding the equals method in the class to provide a custom equals method that correctly compares List[Int] objects. This ensures that objects with the same values are considered equal.

## Contributing
Contributions are welcome. Please feel free to open issues or submit pull requests.