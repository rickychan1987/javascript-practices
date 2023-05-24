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

## Century From Year

```JS
#1:
//remove the given code and insert below in:
const century = year => Math.ceil(year/100)

#2:
function century(year) {
  return Math.ceil(year/100); //using ceiling method to round up to nearest century (100)
}
```

## Cat years, Dog years

```JS
#1:
var humanYearsCatYearsDogYears = function(y) {
  if (y == 1) return [1, 15, 15]
  if (y == 2) return [2, 24, 24]
  return [y, (y-2) * 4 + 24, (y-2) * 5 + 24]
}

#2:
const humanYearsCatYearsDogYears = humanYears => [
  humanYears,
  ( humanYears - 1 ? 16 : 11 ) + 4 * humanYears,
  ( humanYears - 1 ? 14 : 10 ) + 5 * humanYears,
];

```

## Total amount of points

```JS
#1:
const points = g => g.reduce((a, [x, _, y]) => a + (x > y ? 3 : x == y), 0)

#2:
function points(games) {
  let total = 0;
  games.map(game => {
    if (game[0] === game[2]) {
      total += 1;
    } else if (game[0] > game[2]) {
      total += 3;
    }
  });
  return total;
}
```

## Remove String Spaces

```JS
#1:
function noSpace(x){
  return x.replace(/\s/g, '');
}

#2:
function noSpace(x){return x.split(' ').join('')}
```

## Convert a string to an array

```JS
#1:
function stringToArray(string){
  return string.split(' ');
}

#2:
const stringToArray = string => string.split(' ');
```

## String repeat

```JS
#1:
function repeatStr (n, s) {
  return s.repeat(n);
}

#2:
function repeatStr (n, s) {
var str="";
for(var i=0; i < n; i++)
  str+=s;
  return str;
}
```

## Basic Mathematical Operations

```JS
#1:
function basicOp(operation, value1, value2) {
    switch (operation) {
        case '+':
            return value1 + value2;
        case '-':
            return value1 - value2;
        case '*':
            return value1 * value2;
        case '/':
            return value1 / value2;
        default:
            return 0;
    }
}
#2:
function basicOp(o, a, b) {
  return eval(a+o+b);
}
```

## Even or Odd

```JS
#1:
function even_or_odd(number) {
  return number % 2 ? "Odd" : "Even"
}

#2:
function even_or_odd(number) {
  if (number%2 == 0) {
    return "Even";
  } else {
    return "Odd";
  }
}
```

## Counting sheep...

```JS
#1:
function countSheeps(arrayOfSheeps) {
  return arrayOfSheeps.filter(Boolean).length;
}

#2:
function countSheeps(arrayOfSheep) {
  // TODO May the force be with you
  var num = 0;

  for(var i = 0; i < arrayOfSheep.length; i++)
    if(arrayOfSheep[i] == true)
      num++;

  return num;
}

#3:
let countSheeps = x => x.filter( s => s ).length;
```
