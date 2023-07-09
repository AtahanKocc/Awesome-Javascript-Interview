# JS-Interview-Q-A


## Question 1. What will be the output of the following code?

``` javascript
function test1(){
  return{
    name: "Atahan Koc"
  }
}

function test2(){
  return 
  {
    name: "Atahan Koc"
  }
}

console.log(test1());
console.log(test2());
```
<details><summary><b>Answer</b></summary>

{ name: 'Atahan Koc' }
undefined
First, the test1 function is defined. This function returns an object with the name property set to "Atahan Koc".

Next, the test2 function is defined. This function also returns an object, but there is a line break immediately after the return statement. This line break triggers JavaScript's automatic semicolon insertion rule. According to this rule, a semicolon is automatically inserted after the return statement.
The first console.log statement calls the test1() function and prints the returned object. The object is in the form { name: 'Atahan Koc' }.

The second console.log statement calls the test2() function and prints the returned value. However, an important point to note here is that due to the line break after the return statement, JavaScript automatically inserts a semicolon, and the return statement returns an empty value. Therefore, the console.log statement prints undefined.

As a result, the test1() function returns an object { name: 'Atahan Koc' }, while the test2() function returns undefined. This difference arises due to the line break after the return statement in the second function and JavaScript's automatic semicolon insertion rule.

</details>
