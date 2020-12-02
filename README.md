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
```
function depositProfit(deposit, rate, threshold) {
    let sum = 0;
    let years = 0;
    
    while(sum < threshold) {
        sum = sum + (sum*20/100)
        years++;
    }
    return sum;
}
```
