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

The code defines two functions, test1 and test2.

In test1, an object with the name property set to "Atahan Koc" is returned. In test2, a line break after the return statement causes JavaScript's automatic semicolon insertion rule to add a semicolon. As a result, the return statement returns an empty value, leading to undefined being returned.

When test1() is called, it returns an object { name: 'Atahan Koc' }.

When test2() is called, it returns undefined.

The difference in return values arises due to the line break and automatic semicolon insertion in test2.

</details>

## Question 2. What will be the output of the following code?

```javascript
console.log(1<2<3);
console.log(3>2>1); 

```
<details><summary><b>Answer</b></summary>

true
false

First, 1 < 2 is evaluated, which returns true because 1 is less than 2.
Then, true < 3 is evaluated. JavaScript automatically converts logical values to numerical values, with true being converted to 1.
As a result, the expression is evaluated as 1 < 3, which is true.
Therefore, the first console.log prints true.
The second console.log expression evaluates the expression 3 > 2 > 1. It is also evaluated from left to right.

First, 3 > 2 is evaluated, which returns true because 3 is greater than 2.
Then, true > 1 is evaluated. JavaScript automatically converts true to the numerical value 1.
However, it's important to note that 1 > 1 is false because 1 is not greater than 1; it's equal to 1.
Therefore, the expression is evaluated as true > 1, which is false.
As a result, the second console.log prints false.
</details>


##  Question 3: Is there a difference between null and undefined in JavaScript?

<details><summary><b>Answer</b></summary>

JavaScript, unlike some other languages, treats null and undefined as two distinct concepts.

In JavaScript, undefined means that a variable has been declared but has not been assigned a value yet.

On the other hand, null is an assignment value that can be assigned to a variable to represent the absence of a value. When we use the typeof operator on null, it returns "object" indicating that null is considered an empty object reference.

</details>


## Question 4: What will be the output of the following code?

``` javascript
var bar = true;
console.log(bar + 0);   
console.log(bar + "xyz");  
console.log(bar + true);  
console.log(bar + false); 
```

<details><summary><b>Answer</b></summary>

output:
1 <br>
"truexyz" <br>
2 <br>
1 

</details>
