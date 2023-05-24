# 6kyu

## Multiples of 3 or 5:

```JS
#1:
function solution(number){
  var sum = 0;

  for(var i = 1;i< number; i++){
    if(i % 3 == 0 || i % 5 == 0){
      sum += i
    }
  }
  return sum;
}
#2:
function solution(number) {
  let arr = [];
  for (let i = number - 1; i >= 0; i--) {
    if (i % 3 === 0) arr.push(i);
    if (i % 5 === 0) arr.push(i);
  }
  return [...new Set(arr)].reduce((a, b) => a + b, 0);
}
```

## Another one down—the Survival of the Fittest!

```JS
#1:
function removeSmallest(n, arr) {
  if (n<=0) return arr
  if (n>=arr.length) return []
  let i = 0
  arr=arr.slice()
  let sorted = arr.slice().sort((a,b)=>a-b)
  while (n>=1){
    for (let j=0;j<arr.length;j++){
      if (arr[j]===sorted[i]){
        n--
        arr[j]='*'
        i++
        break
      }
    }
  }
  return arr.filter(v=>v!=='*');
}
```

## Create Phone Number

```JS
#1:
function createPhoneNumber(numbers){
  var format = "(xxx) xxx-xxxx";

  for(var i = 0; i < numbers.length; i++)
  {
    format = format.replace('x', numbers[i]);
  }

  return format;
}

#2:
function createPhoneNumber(numbers){
  numbers = numbers.join('');
  return '(' + numbers.substring(0, 3) + ') '
      + numbers.substring(3, 6)
      + '-'
      + numbers.substring(6);
}
```
