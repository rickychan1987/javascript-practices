# 7kyu:

## Get Planet Name By ID

```JS
#1: just add 'break;' at bottom each of case as standard swtch case built in javascripts.

#2: cleaver one adjust those case being an object.
function getPlanetName(id){
  return {
    1: 'Mercury',
    2: 'Venus',
    3: 'Earth',
    4: 'Mars',
    5: 'Jupiter',
    6: 'Saturn',
    7: 'Uranus',
    8: 'Neptune'
  }[id]
}
```

## Multiply

```JS
#1:
function multiply(a, b) {
  return a * b;
}

#2: using arrow function.
const multiply = (a, b) => a * b;
```

## Reversed Strings

```JS
#1: this answer must use Array built-in function with 3 methods which are: array.split(""), array.reverse(),array,join("")
function solution(str){
const arr = str.split("");
const reversed = arr.reverse();
const finalAnswer = reversed.join("");
return finalAnswer;
}

#2: with this type of answer we can save many code there.
function solution(str){
return str.split("").reverse().join("");
}
```
