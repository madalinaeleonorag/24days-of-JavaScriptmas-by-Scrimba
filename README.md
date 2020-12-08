# 24 days of #JavaScriptmas

Level up JavaScript skills with a daily coding challenge from December 1st to 24th.

Challenge available [HERE](https://scrimba.com/learn/adventcalendar)


1. Candies<br>
Determine how many pieces of candy will be eaten by all te children together

Solution:
```javascript
function candies(children, candy) {
    return Math.floor(candy/children) * children;
}
```

2. Deposit Profit<br>
Find out how long it would take for your balance to pass a specific treshold with the assumption that you don't make any additional deposit

Solution:
```javascript
function depositProfit(deposit, rate, threshold) {
    let sum = deposit;
    let years = 0;
    
    while(sum < threshold) {
        sum = sum + (sum*20/100)
        years++;
    }
    return years;
}
```

3. Chunky Monkey<br>
Write a function that splits an array into groups the same length of size and returns them as a two-dimensional array

Solution:
```javascript
function chunkyMonkey(values, size) {
    return ([[...values.slice(0, size)],[...values.slice(size, values.length)]]);
}
```

4. Century from year<br>
Given a year, return a century it is in.

Solution:
```javascript
function centuryFromYear(num) {
    return Math.ceil(num/100) 
}
```

5. Reverse a stringr<br>
Reverse the provided string.

Solution:
```javascript
function reverseAString(str) {
    return str.split("").reverse().join('')
}
```

6. Sort by length<br>
Given an array of strings, sort them in the order of increasing lengths. 

Solution:
```javascript
function sortByLength(strs) {
   return strs.sort((a, b) => a.length - b.length)
}
```

7. Count vowel consonant<br>
Return the sum of all letters in the input string.

Solution:
```javascript
function countVowelConsonant(str) {
  const vowels = ['a', 'e', 'i', 'o', 'u'];
  const chars = str.split('');
  return total = chars.reduce((acc, char) => {
      if(vowels.includes(char)) {
          return acc + 1;
      }
      return acc + 2;
  }, 0);
}
```

8. Rolling dice<br>
In this challenge a casino has asked you to make an online dice that works just like it would in real life. Using the pre-made dice face that represents ‘one’, make the faces for ‘two’, ‘three’, ‘four’, ‘five’ and ‘six’. Now when the users clicks the dice on the screen the dice is expected to show one of the faces randomly.

Solution:
```HTML
<html>
    <head>
        <link rel="stylesheet" href="style.css">
        <script src="index.pack.js"></script>
    </head>
    <body>
        <div class="dice">
            <div class="dots dot"></div>
        </div>
    </body>
</html>
```
```javascript
const dice = document.querySelector('.dice');
const dots = document.querySelector('.dots');
const dotsClasses = ["dot", "dot2", "dot3", "dot4", "dot5"];
let lastDots = "dot";

function rollDice() {
    dots.classList.remove(lastDots);
    const randomClass = dotsClasses[Math.floor((Math.random() * 5))];
    if (randomClass === lastDots) return;
    
    lastDots = randomClass;
    dots.classList.add(randomClass);
}

dice.addEventListener('click', rollDice);
```CSS
body {
    background-color: #AEB8FE;
    display: flex;
}

.dice {
    width: 100px;
    height: 100px;
    border-radius: 10px;
    background-color: #EFE5DC;
    margin: 100px;
}

.dots {
    width: 15px;
    height: 15px; 
    margin: 40px;      
}

.dot {
    background-color: black;
}

.dot2 {
    background-color: red;
}

.dot3 {
    background-color: yellow;
}

.dot4 {
    background-color: green;
}

.dot5 {
    background-color: purple;
}
```
