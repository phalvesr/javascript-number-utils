# javascript-number-utils

#### Get Fibonacci numbers
```
Number.__proto__.getFibonacciNumbersLessThanOrEqualsTo = function(number) {
  
  number = parseInt(number);

    if (number <= 0) return NaN;
    if (number === 1) return [1];

    const fibonacciNumbers = [1, 1];
    let lastFibonacciNumber = 0;
    let index = 1;

    while (lastFibonacciNumber <= number) {

      const next = fibonacciNumbers[index] + fibonacciNumbers[index - 1];
      index++;

      if (next > number) {
        break;
      }
      
      fibonacciNumbers.push(next);

      lastFibonacciNumber = next;
    }

    return fibonacciNumbers;
}
```
