# Loop Exercises

1. Write a `while` loop and a `for` loop that takes the variable "num" and logs all the numbers, descending, between "num" and 1.
```
let num = 9
while (num > 1) {
  console.log(num)
  num -= 1
}
```
```
for (let num = 10; num > 0; num -= 1) {
  console.log(num)
}

```

2. Write a `while` loop and a `for` loop that takes the variable "num", and iterates over all numbers from 0 to "num".
For each iteration, it will check if the current number is even or odd, and log that to the screen (e.g. "2 is even")
```
let num = 0;
while(num <= 10) {
 if(num % 2 === 0) {
   console.log(num + ' This is even')
 } else if (num % 1 === 0){
   console.log(num + ' This is odd')
 }
 num++
}
```
```
for (let i = 0; i <= 15; i++){
  if (i % 2 === 0){
    console.log(i + ' This is even')
  } else {
    console.log(i + ' This is odd')
  }
}
```

3. Write a `while` loop and a `for` loop that takes the variable "num" and iterates over all numbers from 0 to "num".
For each iteration of the loop, it will multiply the number by 9 and log the result (e.g. "2 * 9 = 18").
```
let num = 0;
while(num <= 10) {
 console.log(num + ' * 9 = ' + num * 9)
 num++
}
```
```
for (let i = 0; i <= 15; i++){
  console.log(i + " * 9 = " + i * 9)
}
```

_Bonus_ think of another way to solve it.
  <details>
    <summary>
      Hint
    </summary>
    Find the final number and increment the loop by 9.
  </details>

4. Write a loop that uses console.log to log all the numbers from 1 to 100, with two exceptions. For numbers divisible by 3, log "Fizz" instead of the number, and for numbers divisible by 5 (and not 3), log "Buzz" instead.
```
for (let i = 0; i <= 100; i++){
  if (i % 3 === 0){
    console.log(i + ' fizz')
  } else if (i % 5 === 0) {
    console.log(i + ' buzz')
  } else {
    console.log(i)
  }
}
```

5. Modify your program to log "FizzBuzz", for numbers that are divisible by both 3 and 5 (still log "Fizz" or "Buzz" for numbers divisible by only one of those).
```
for (let i = 0; i <= 100; i++){
   if (i % 5 === 0 && i % 3 === 0){
    console.log(i + ' fizz')
  } else if (i % 5 === 0) {
    console.log(i + ' buzz')
  } else if (i % 3 === 0){
    console.log(i + ' fizzbuzz')
  } else {
    console.log(i)
  }
}
```

Bonus:

1. Write a program that would log the lyrics of the song 99 Bottles of Beer. This is the first verse of the song:

99 bottles of beer on the wall,

99 bottles of beer.

Take one down, pass it around,

98 bottles of beer on the wall.

This verse is repeated, each time with one less bottle, until the number of bottles is 0. When the number of bottles is 2, the verse is:

2 bottles of beer on the wall,

2 bottles of beer.

Take one down, pass it around,

1 bottle of beer on the wall.

In the last line, the word bottles (plural), is  replaced with bottle (singular)

When the number of bottles is 1, the verse is:

1 bottle of beer on the wall,

1 bottle of beer.

Take one down, pass it around,

No more bottle of beer on the wall.
```
let bottle = ' bottles of beer on the wall, '
let bottle2 = ' bottles of beer. '
let take = 'Take one down, pass it around, '
for (let beer = 99; beer >= 1; beer --){
  if (beer === 1 ){
    console.log('\n' + beer + ' bottle of beer on the wall, ' + beer + ' bottle of beer. ' + '\n' + '\n' + take + '\n' + '\n' + 'no more bottles of beer on the wall')
  } else if (beer === 2){
    console.log('\n' + beer + bottle + beer + bottle2 + '\n' + '\n' + take + (beer - 1) + ' bottle of beer on the wall.')
  } else {
    console.log('\n' + beer + bottle + beer + bottle2 + '\n' + '\n' + take + (beer -1) + bottle.slice(0,28)+'.')
  }
}
```



2. Use the assignGrade function (given below). Write a function that logs each number from 60 - 100 along with its corresponding letter score.
Exp For each number from 81 to 90, log B, like so:

```js
81 - B
82 - B
83 - B
...
```

```js
function assignGrade(score) {
    if (score > 90) {
        return 'A';
    } else if (score > 80) {
        return 'B';
    } else if (score > 70) {
        return 'C';
    } else if (score > 65) {
        return 'D';
    } else {
        return 'F';
    };
};
```
```
for (let assignGrade = 100; assignGrade >= 0; assignGrade --)
if (assignGrade > 89){
  console.log(assignGrade + ' - A')
} else if (assignGrade > 79){
  console.log(assignGrade + ' - B')
} else if (assignGrade > 69){
  console.log(assignGrade + ' - C')
} else if (assignGrade > 64){
  console.log(assignGrade + ' - D')
} else {
  console.log(assignGrade + ' - F')
}
```
