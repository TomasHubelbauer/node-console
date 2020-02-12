# Overriding `console.log` in Node

## Running

`node .`

## Usage

```javascript
const consoleLog = console.log;

console.log = function (message, ...optionalParams) {
  consoleLog('>> Logging:');
  consoleLog('>>', message, ...optionalParams);
  consoleLog('>> Logged!:');
};

console.log('one', 2, 'three', 4);

console.log = consoleLog;

console.log('one', 2, 'three', 4);
```
