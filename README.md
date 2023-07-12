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

###  Question 5: What would be the output of following code?
```javascript
var arrA = [0,1,2,3,4,5];
var arrB = arrA.slice();
arrB[0]=42;
console.log(arrA)
```


<details><summary><b>Answer</b></summary>

The output will be `[0,1,2,3,4,5]`. 

The `slice` function copies all the elements of the array returning the new array. That's why
`arrA` and `arrB` reference two completely different arrays. 

</details>

##  Question 6: What is the usage of Void(0)?

<details><summary><b>Answer</b></summary>
Void(0) is used to prevent the page from refreshing, and it passes the parameter "zero" during the execution.
</details>


## Question 7:  What are JavaScript Data Types?

<details><summary><b>Answer</b></summary>

Following are the JavaScript Data types:

- Number
- String
- Boolean
- Object
- Undefined

</details>

## Question 8: What are all the types of Pop up boxes available in JavaScript?

<details><summary><b>Answer</b></summary>

- alert
- confirm
- prompt

</details>

## Question 9: What is progressive rendering?

<details><summary><b>Answer</b></summary>

Progressive rendering is an approach in web development that focuses on displaying content to users as quickly as possible, even before the entire web page has finished loading.

</details>


## Question 10:  Why do we use the word “debugger” in javascript?

<details><summary><b>Answer</b></summary>
The debugger for the browser must be activated in order to debug the code. Built-in debuggers may be switched on and off, requiring the user to report faults. The remaining section of the code should stop execution before moving on to the next line while debugging.

</details>

## Question 11:  Difference between “ == “ and “ === “ operators.

<details><summary><b>Answer</b></summary>
The "==" operator is used to compare values, while the "===" operator is used to compare both values and types.
</details>

## Question 12:  What are object prototypes?

<details><summary><b>Answer</b></summary>
Date objects inherit properties from the Date prototype
Math objects inherit properties from the Math prototype
Array objects inherit properties from the Array prototype.
</details>


## Question 13: What are callbacks?

<details><summary><b>Answer</b></summary>
A callback is a function that will be executed after another function gets executed. In javascript, functions are treated as first-class citizens, they can be used as an argument of another function, can be returned by another function, and can be used as a property of an object.
</details>

## Question 14: What would be the output of following code ?
``` javascript
(function() {
	var objA = {
		foo: 'foo',
		bar: 'bar'
	};
	var objB = {
		foo: 'foo',
		bar: 'bar'
	};
	console.log(objA == objB);
	console.log(objA === objB);
}()); 
```

a. false true
b. false false
c. true  true
d. true  false


<details><summary><b>Answer</b></summary>
b. false false
</details>

## Question 15: What would be the output of following code ?
``` javascript
(function() {
	var objA = {
		foo: 'foo'
	};
	var objB = objA;
	objB.foo = 'bar';

	delete objA.foo;
	console.log(objA.foo);
	console.log(objB.foo);
}());

```

<details><summary><b>Answer</b></summary>
Inside the function, objA is defined as an object with a foo property set to "foo".

objB is then assigned the reference of objA, so both objA and objB point to the same object.

The value of objB.foo is changed to "bar". Since both objA and objB reference the same object, this change affects both variables.

The foo property is deleted from objA.

The first console.log statement evaluates objA.foo. Since the foo property was deleted, its value is undefined.

The second console.log statement evaluates objB.foo. Since objB still refers to the modified object, the value of foo is "bar".

In summary, the first console.log outputs undefined because the foo property was deleted from objA, while the second console.log outputs "bar" because objB still refers to the modified object.
</details>


## Question 16: What would be the output of following code ?

```javascript
let arrayIntegers = [1, 2, 3, 4, 5];
let arrayIntegers1 = arrayIntegers.slice(0, 2); 
let arrayIntegers2 = arrayIntegers.slice(2, 3); // returns [3]
let arrayIntegers3 = arrayIntegers.slice(4); //returns [5]

```
<details><summary><b>Answer</b></summary>
// returns [1,2]
// returns [3]
// returns [5]
</details>


## Question 17: What is a first order function?

<details><summary><b>Answer</b></summary>
First-order function is a function that doesn’t accept another function as an argument and doesn’t return a function as its return value.
````javascript
const firstOrder = () => console.log("I am a first order function!");
```
</details>


## Question 18: Why do you need modules?

<details><summary><b>Answer</b></summary>
Below are the list of benefits using modules in javascript ecosystem

Maintainability
Reusability
Namespacing
</details>


## Question 19: . What is the output of below code?
```javascript 
console.log("🙂" === "🙂");
```

<details><summary><b>Answer</b></summary>
true
</details>


## Question 20: What is the output of below code?

``` javascript
console.log(typeof typeof typeof true);
```

1: string
2: boolean
3: NaN
4: number
<details><summary><b>Answer</b></summary>
1: string
</details>


## Question 21: What is the output of below code?
``` javascript
let zero = new Number(0);

if (zero) {
  console.log("If");
} else {
  console.log("Else");
}
```
A: If 
B: Else
C: NaN
D: SyntaxError

<details><summary><b>Answer</b></summary>
 A: If
</details>

## Question 22: What is the output of the below code?

``` javascipt
let count = 10;

(function innerFunc() {
  if (count === 10) {
    let count = 11;
    console.log(count);
  }
  console.log(count);
})();
```
<details><summary><b>Answer</b></summary>
 11, 10
</details>


## Question 23:

``` javascript
getMessage();

var getMessage = () => {
  console.log("Good morning");
};

```
A: Good morning <br>
B: getMessage is not a function <br>
C: getMessage is not defined  <br>
D: Undefined

<details><summary><b>Answer</b></summary>
 B : getMessage is not a function
</details>


## Question 24: What is the output of the below code?
```javascript
const resp = () => {
    return (()=> 0 )();
}
console.log("typeof : "+ typeof resp())

```

<details><summary><b>Answer</b></summary>
typeof : number
</details>

## Question 25: What does "NaN" mean in JavaScript?

<details><summary><b>Answer</b></summary>
"NaN" stands for "Not a Number." It is used to indicate an invalid number result when performing a mathematical operation in JavaScript.
</details>

## Question 26: What is "prototype" in JavaScript and how is it used?

<details><summary><b>Answer</b></summary>
"Prototype" is a feature in JavaScript used to share properties and methods among objects. When an object is created, its properties and methods can be accessed through the prototype chain.
</details>


## Question 27: What is a "Promise" in JavaScript and how does it work?

<details><summary><b>Answer</b></summary>
"Promise" is a construct used to manage asynchronous operations in JavaScript. It returns an object that represents the eventual completion or failure of an asynchronous operation and provides a way to handle the returned value. "Promise" is used with the "then()" and "catch()" methods to perform relevant actions when the operation is successful or when an error occurs.
</details>





