# sol-eye
Find all calls to import in your solidity code using a Depth-first traversal of the code's Abstract Syntax Tree.
```sol-eye``` takes solidity code as input and outputs a list of all files the code is importing from, regardless of where the ```import``` exists inside your code.

Inspired by [node-detective](https://github.com/substack/node-detective)

#Install
```bash
npm install --save sol-eye
```

#Usage
```js
let eye = require ('sol-eye'),
  code = 'import * as chua from "lannister.sol";\n\ncontract Cas {\nimport "baratheon.sol";\n\nfunction cd () {\nimport {a,b,c} from "stormborn.sol";\n}\n}';
  
console.log (
  eye.version + '\n',
  eye.findImports (code)
);
```

#Output
```js
[ 'lannister.sol', 'baratheon.sol', 'stormborn.sol' ]
```

#Future Enhancement(s)

1. Browser Support
