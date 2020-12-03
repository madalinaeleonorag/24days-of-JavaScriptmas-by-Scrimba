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
