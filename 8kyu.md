# 8kyu:

## Beginner - Lost Without a Map

```JS
1st:
function map(x){
    return x.map(n => n * 2)
}

2nd:
function maps(x){
//return x.map(el => el * 2);   #you can ignore this
let arr = [];
for(let i = 0; i < x.length; i++){
arr.push(x[i] * 2);
}
return arr;
}
```

## Counting Sheep

```JS
#1
function countSheeps(arrayOfSheep) {
  return arrayOfSheep.filter((x) => x === true).length;
}
#2
const countSheeps = (arrayOfSheep) => arrayOfSheep.filter((x) => x).length;
#3
const countSheeps = (arrayOfSheep) => arrayOfSheep.filter(Boolean).length;
```

## Even or Odd

```JS
#1
const even_or_odd = (number) => (number % 2 ? 'Odd' : 'Even');

#2
const even_or_odd = (n) => ['Even', 'Odd'][n & 1];

#3
function even_or_odd(number) {
  if (number % 2 === 0) {
    return "Even";
  } else {
    return "Odd";
  }
}
```

## Find the smallest integer in the array

```JS
class SmallestIntegerFinder {
  #1
  findSmallestInt(args) {
    return args.sort((a, b) => a - b)[0];
  }

  #2
  findSmallestInt(args) {
    return Math.min(...args);
  }
}
```

## Grasshopper-Summation

```JS
#1: Let's start with loopsolutions.
var summation = function (num) {
    let sum = 0
    for(let i = 0; i <= num; i++) {
        sum += i
    }
    return sum
}

#2: Let's solve it with Gauss Formula.
var summation = function (num) {
    return num * (num + 1) / 2
}

#3: Let's solve it with reduce().
var summation = function (num) {
    return Array(num).fill(0).reduce((acc, _, index) => acc + index + 1, 0)
}

#4: Let's solve it with recursion.
var summation = function (num) {
    return num ? num + summation(num - 1) : num
}
```

## Jenny's secret message

```JS
#1: use if else methods to check whether the input variable 'name' is Johnny
function greet(name){
if(name === "Johnny"){
return "Hello, my love!";
} else {
return "Hello, " + name + "!";
}
}

#2: use '?' and ':' as if else for instead.
function greet(name){
return "Hello, " + (name == "Johnny" ? "my love" : name) + "!";
}
```

## Remove First and Last Character

```JS
#1:
function removeChar(str) {
return str.slice(1, -1);
}

#2:
function removeChar(str){
return str.slice(1, str.length - 1);
};

#3:
const removeChar = str => str.slice(1,-1)

#4:
function removeChar(str){
return str.substring(1, str.length-1);
};
```

## Return Negative

```JS
#1: Use if else statement to get back the value of
function makeNegative(num) {
if (num < 0) {
return num;
} else {
return (num = num \* -1);
}
}

#2
function makeNegative(num) {
if (num < 0) {
return num;
} else {
return -num;
}
}

#3
function makeNegative(num) {
return num < 0 ? num : -num;
}

#4
const makeNegative = (num) => (num < 0 ? num : -num);

#5
const makeNegative = (num) => -Math.abs(num);
```

## Rocky Paper Scissors

```JS
#1:
const rps = (p1, p2) => {
if (p1 == p2)
return 'Draw!';

if (p1 == 'rock' && p2 == 'scissors')
return 'Player 1 won!'
else if (p1 == 'scissors' && p2 == 'paper')
return 'Player 1 won!'
else if (p1 == 'paper' && p2 == 'rock')
return 'Player 1 won!'
else
return 'Player 2 won!';
};

#2:
const rps = (p1, p2) => {
if (p1 === p2) return "Draw!";
var rules = {rock: "scissors", paper: "rock", scissors: "paper"};
if (p2 === rules[p1]) {
return "Player 1 won!";
}
else {
return "Player 2 won!";
}
};
```
