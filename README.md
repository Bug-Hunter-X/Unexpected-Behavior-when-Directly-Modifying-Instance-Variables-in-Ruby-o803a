# Unexpected Behavior when Directly Modifying Instance Variables in Ruby

This example demonstrates a potential issue in Ruby when directly manipulating instance variables using `instance_variable_set` instead of using accessor methods. Directly modifying instance variables can lead to unexpected behavior and make code less maintainable.

## Bug Report
The `bug.rb` file showcases how accessing instance variables directly can bypass the intended behavior of the class.  Changes made through `instance_variable_set` are not reflected in any potential validation or logic within the accessor methods, potentially causing inconsistencies and making debugging more difficult. 

## Solution
The `bugSolution.rb` file presents a better approach.  Instead of directly manipulating the `@value` instance variable, it leverages accessor methods (`value=` and `value`) to manage the value, ensuring any logic within those methods is executed.