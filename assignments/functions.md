1. 🎖Write a function named calculateDogAge that:
  * [ ] Takes 1 argument: your puppy's age.
  * [ ] Calculates your dog's age based on the conversion rate of 1 human year to 7 dog years.
  * [ ] Outputs the result to the screen like so: "Your doggie is NN years old in dog years!"
  * [ ] Add an additional argument to the function that takes the conversion rate of human to dog years.

```js
// your code goes here
function calculateDogAge(puppyAge, conversionRate) {
  console.log(`Your doggie is ${puppyAge * conversionRate} years old in dog years!`)
}
```
2. 🎖Write a function named calculateSupply that:
  * [ ] takes 2 arguments: age, amount per day.
  * [ ] calculates the amount consumed for rest of the life (based on a constant max age).
  * [ ] outputs the result to the screen like so: "You will need NN to last you until the ripe old age of X"
  * [ ] Accept floating point values for amount per day, and round the result to a round number.

```js
// your code goes here
function calculateSupply(age, amount) {
  const MAX_AGE = 60;
  console.log(`You will need ${Math.round((MAX_AGE - age) * 365 * amount)} to last you until the ripe old age of ${MAX_AGE}`);
}
```
3. 🎖Create a function called celsiusToFahrenheit:
  * [ ] Store a celsius temperature into a variable.
  * [ ] Convert it to fahrenheit and output "NN°C is NN°F".
  * [ ] Create a function called fahrenheitToCelsius:
  * [ ] Now store a fahrenheit temperature into a variable.
  * [ ] Convert it to celsius and output "NN°F is NN°C."

```js
// your code goes here
function celsiusToFahrenheit(celsiusTemperature) {
  let fahrenheit = 9 / 5 * celsiusTemperature + 32;
  return `${celsiusTemperature}\xB0C is ${fahrenheit.toFixed(2)}\xB0F`;
}

function fahrenheitToCelsius(fahrenheitTemperature) {
  let celsius = (fahrenheitTemperature - 32) * (5/9);
  return `${fahrenheitTemperature}\xB0F is ${celsius.toFixed(2)}\xB0C`
}
```
4. 🎖The function below returns true if the parameter age is greater than 18. Otherwise it asks for a confirmation and returns its result:

```js
function checkAge(age) {
  if (age > 18) {
    return true;
  } else {
    // ...
    return confirm("Did parents allow you?");
  }
}
```
  4.1 🎖Convert the above function using ternary operator.
  ```js
  // your code goes here
  function checkAge(age) {
    return age > 18 ? true : confirm("Did parents allow you?");
  }
  ```

  4.2 🎖Convert the above function using `||` operator.
  ```js
  // your code goes here
  function checkAge(age) {
    return age > 18 || confirm("Did parents allow you?");
  }
  ```
Will the function work differently if else is removed like below?

```js
function checkAge(age) {
  if (age > 18) {
    return true;
  }
  // ...
  return confirm("Did parents allow you?");
}
//There is no difference in the behaviour of these two variants, if block if it gets executed then it will return true and come out of 
//function whereas if block is false in that case the next return statement will get executed thus keeping the behaviour intact.
```
Is there any difference in the behavior of these two variants? If there is what is that?



5. 🎖 Write a function pow(x,n) that returns x in power n.

  * [ ] Use prompt to take values for x and n, and then shows the result of pow(x,n) using alert.
  * [ ] In this task the function should support only natural values of n: integers greater then 1.

```js
// Your code goes here
let x = +prompt("Input the value of x ", "");
let n = Math.floor( +prompt("Input the value of n ", "") );

pow(x,n);

function pow(x, n) {
  if(n < 1 || x < 1) return `The number below 1 is not allowed`;
  alert("Result " + x ** n)
}

// After writing code uncomment to check the answer.
// pow(3, 2); // 9
// pow(3, 3); // 27
// pow(1, 100); // 1
// pow(-31, 2); // "The number below 1 is not allowed"

6. 🎖Write a program that asks the user for a number n and gives them the possibility to choose between computing the sum and computing the product of 1,…,n. Return the result accordingly.

```js
// your code goes here
let n = +prompt("Enter a number")
let operation = prompt("Choose between computing the sum and product. For sum input as + and for product input as *")
function sumProduct(n, operation) {
  if (operation === "+"){
    let sum = 0;

    for(let i = 0; i <= n; i++) {
      sum += i;
    }

    return sum;
  } else if (operation === "*") {
    let product = 1;

    for(let i = 1; i <= n ; i++) {
      product *= i;
    }

    return product;
  } else {
    return `Please enter the valid operation, it can be either + or *`;
  }
}

console.log(sumProduct(n, operation))
```
6. 🎖Write a program that asks the user for a number n using prompt and prints the sum of the numbers 1 to n

```js
// your code goes here
let n = +prompt("Enter a number ", "");
function sum(n) {
  let sumValue = 0;
  
  for(let i = 1;i <= n; i++) {
    sumValue += i;
  }
  
  return sumValue
}

console.log(sum(n))
```
7. 🎖Modify the previous program such that only multiples of 5 or 7 are considered in the sum, e.g. n = 20 (5,7,10,14,15,20) 71

```js
// your code goes here
let n = +prompt("Enter a number ", "");
function sum(n) {
  let sumValue = 0;
  
  for(let i = 1;i <= n; i++) {
    if(i % 5 === 0 || i % 7 === 0) {
      sumValue += i ;
    }
  }
  
  return sumValue
}

console.log(sum(n))
```

8. 🎖Write a function `min` that takes two arguments and returns their minimum.

```js
// Your code here.

function min(num1, num2) {
  return num1 < num2 ? num1 : num2
}

console.log(min(0, 10));
// → 0
console.log(min(0, -10));
// → -10
```