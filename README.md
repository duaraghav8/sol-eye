# sol-eye
Find all calls to import in your solidity code using a Depth-first traversal of the code's Abstract Syntax Tree.
```sol-eye``` takes solidity code as input and outputs a list of all files the code is importing from, regardless of where the ```import``` exists inside your code.

Inspired by [node-detective](https://github.com/substack/node-detective)


