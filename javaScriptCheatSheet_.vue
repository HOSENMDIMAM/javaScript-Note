<script>
//source 
//https://www.doabledanny.com/javascript-array-cheat-sheet
//https://htmlcheatsheet.com/js/


// setInterval for continus every second
setTimeout(function () {
    console.log("print after 1 second");
}, 1000);

function addNumbers(a, b) {
return a + b; //3
}
console.log(addNumbers(1, 2));

//_____Output_____
console.log(a);             // write to the browser console
document.write(a);          // write to the HTML
alert(a);                   // output in an alert box
confirm("Really?");         // yes/no dialog, returns true/false depending on user click
prompt("Your age?","0");    // input dialog. Second argument is the initial value

// _________Loops___________
let sum = 0;
for (let i = 0; i < a.length; i++) {
    sum += a[i];
} 
// _______Break & Continue_______
for (var i = 0; i < 10; i++) {
    if (i == 5) { break; }          // stops and exits the cycle
    document.write(i + ", ");       // last output number is 4
}
for (var i = 0; i < 10; i++) {
    if (i == 5) { continue; }       // skips the rest of the cycle
    document.write(i + ", ");       // skips 5
}
// _________If & Else________
if ((age >= 14) && (age < 19)) {        // logical condition
    return "Eligible.";               // executed if condition is true
} else {                                // else block is optional
    return "Not eligible.";           // executed if condition is false
}
// _________Switch__________
switch (new Date().getDay()) {      // input is current day
case 6:                         // if (day == 6)
	text = "Saturday";          
	break;
case 0:                         // if (day == 0)
	text = "Sunday";
	break;
default:                        // else...
	text = "Whatever";
}
// __________Variables__________
let  a;                          // variable
let b = "init";                 // string
let c = "Hi" + " " + "Joe";     // = "Hi Joe"
let d = 1 + 2 + "3";            // = "33"
let e = [2,3,5,8];              // array
let f = false;                  // boolean
let g = /()/;                   // RegEx
let h = function(){};           // function object
const PI = 3.14;                // constant
const x = 1, y = 2, z = x + y;    // one line
let zz = 'zzz';                  // block scope local variable

// __________Strict mode__________
"use strict";   // Use strict mode to write secure code
x = 1;          // Throws an error because variable is not declared
// _______Values_______
false, true                     // boolean
18, 3.14, 0b10011, 0xF6, NaN    // number
"flower", 'John'                // string
undefined, null , Infinity      // special

// Operators
a = b + c - d;      // addition, substraction
a = b * (c / d);    // multiplication, division
x = 100 % 48;       // modulo. 100 / 48 remainder = 4
a++; b--;           // postfix increment and decrement

// ________Bitwise operators_______
/* &	AND 	 5 & 1 (0101 & 0001)	1 (1)
   |	OR 	     5 | 1 (0101 | 0001)	5 (101)
   ~	NOT 	 ~ 5 (~0101)	10 (1010) */

//_______Arithmetic_______
a * (b + c)         // grouping
person.age          // member
person[age]         // member
!(a == b)           // logical not
a != b              // not equal
typeof a            // type (number, object, function...)
a = b               // assignment
a == b              // equals
a != b              // unequal
a === b             // strict equal
a !== b             // strict unequal
a < b   a > b       // less and greater than
a <= b  a >= b      // less or equal, greater or eq
a += b              // a = a + b (works with - * %...)
a && b              // logical and
a || b              // logical or

// _________Data Types________
var age = 18;                           // number 
var name = "Jane";                      // string
var name = {first:"Jane", last:"Doe"};  // object
var truth = false;                      // boolean
var sheets = ["HTML","CSS","JS"];       // array
var a; typeof a;                        // undefined
var a = null;                           // value null

// __________Objects__________
var student = {                 // object name
    firstName:"Jane",           // list of properties and values
    lastName:"Doe",
    age:18,
    height:170,
    fullName : function() {     // object function
    return this.firstName + " " + this.lastName;
    }
}; 
student.age = 19;           // setting value
student[age]++;             // incrementing
name = student.fullName();  // call object function

// _______String___________
var abc = "abcdefghijklmnopqrstuvwxyz";
var esc = 'I don\'t \n know';   // \n new line
var len = abc.length;           // string length
abc.indexOf("lmno");            // find substring, -1 if doesn't contain 
abc.lastIndexOf("lmno");        // last occurance
abc.slice(3, 6);                // cuts out "def", negative values count from behind
abc.replace("abc","123");       // find and replace, takes regular expressions
abc.toUpperCase();              // convert to upper case
abc.toLowerCase();              // convert to lower case
abc.concat(" ", str2);          // abc + " " + str2
abc.charAt(2);                  // character at index: "c"
abc[2];                         // unsafe, abc[2] = "C" doesn't work
abc.charCodeAt(2);              // character code at index: "c" -> 99
abc.split(",");                 // splitting a string on commas gives an array
abc.split("");                  // splitting on characters
128.toString(16);               // number to hex(16), octal (8) or binary (2)

// ________Numbers and Math∑________
var pi = 3.141;
pi.toFixed(0);          // returns 3
pi.toFixed(2);          // returns 3.14 - for working with money
pi.toPrecision(2)       // returns 3.1
pi.valueOf();           // returns number
Number(true);           // converts to number
Number(new Date())      // number of milliseconds since 1970
parseInt("3 months");   // returns the first number: 3
parseFloat("3.5 days"); // returns 3.5
Number.MAX_VALUE        // largest possible JS number
Number.MIN_VALUE        // smallest possible JS number
Number.NEGATIVE_INFINITY// -Infinity
Number.POSITIVE_INFINITY// Infinity

// __________Math.____________
var pi = Math.PI;       // 3.141592653589793
Math.round(4.4);        // = 4 - rounded
Math.round(4.5);        // = 5
Math.pow(2,8);          // = 256 - 2 to the power of 8
Math.sqrt(49);          // = 7 - square root 
Math.abs(-3.14);        // = 3.14 - absolute, positive value
Math.ceil(3.14);        // = 4 - rounded up
Math.floor(3.99);       // = 3 - rounded down
Math.sin(0);            // = 0 - sine
Math.cos(Math.PI);      // OTHERS: tan,atan,asin,acos,
Math.min(0, 3, -2, 2);  // = -2 - the lowest value
Math.max(0, 3, -2, 2);  // = 3 - the highest value
Math.log(1);            // = 0 natural logarithm 
Math.exp(1);            // = 2.7182pow(E,x)
Math.random();          // random number between 0 and 1
Math.floor(Math.random() * 5) + 1;  // random integer, from 1 to 5

// ________Dates📆________
//Sat Nov 12 2022 15:23:30 GMT+0900 (Japan Standard Time)
let d = new Date();
1668234210200 miliseconds passed since 1970
Number(d) 
Date("2017-06-23");                 // date declaration
Date("2017");                       // is set to Jan 01
Date("2017-06-23T12:00:00-09:45");  // date - time YYYY-MM-DDTHH:MM:SSZ
Date("June 23 2017");               // long date format
Date("Jun 23 2017 07:45:00 GMT+0100 (Tokyo Time)"); // time zone

// ____________Get Times_________
let d = new Date();
a = d.getDay();     // getting the weekday

getDate();          // day as a number (1-31)
getDay();           // weekday as a number (0-6)
getFullYear();      // four digit year (yyyy)
getHours();         // hour (0-23)
getMilliseconds();  // milliseconds (0-999)

// ________Setting part of a date_________
let d = new Date();
d.setDate(d.getDate() + 7); // adds a week to a date

setDate();          // day as a number (1-31)
setFullYear();      // year (optionally month and day)
setHours();         // hour (0-23)
setMilliseconds();  // milliseconds (0-999)

// _________Arrays≡__________
let dogs = ["Bulldog", "Beagle", "Labrador"]; 
let dogs = new Array("Bulldog", "Beagle", "Labrador");  // declaration

alert(dogs[1]);             // access value at index, first item being [0]
dogs[0] = "Bull Terier";    // change the first item

for (let i = 0; i < dogs.length; i++) {     // parsing with array.length
    console.log(dogs[i]);
}

// ________ Methods___________
dogs.toString();                        // convert to string: results "Bulldog,Beagle,Labrador"
dogs.join(" * ");                       // join: "Bulldog * Beagle * Labrador"
dogs.pop();                             // remove last element
dogs.push("Chihuahua");                 // add new element to the end
dogs[dogs.length] = "Chihuahua";        // the same as push
dogs.shift();                           // remove first element
dogs.unshift("Chihuahua");              // add new element to the beginning
delete dogs[0];                         // change element to undefined (not recommended)
dogs.splice(2, 0, "Pug", "Boxer");      // add elements (where, how many to remove, element list)
let animals = dogs.concat(cats,birds);  // join two arrays (dogs followed by cats and birds)
dogs.slice(1,4);                        // elements from [1] to [4-1]
dogs.sort();                            // sort string alphabetically
dogs.reverse();                         // sort string in descending order
x.sort(function(a, b){return a - b});   // numeric sort
x.sort(function(a, b){return b - a});   // numeric descending sort
highest = x[0];                         // first item in sorted array is the lowest (or highest) value
x.sort(function(a, b){return 0.5 - Math.random()});     // random order sort

// _________17 commonly used array methods:_______
/*In JavaScript, all arrays are constructed from the global Array class.
 All array methods are stored in the Array.prototype object.*/

Array.prototype.toString                // Converts an array into a string of comma-separated array values:
let names = ["Zoe", "Adam", "Dan"]
let strNames = names.toString()         // Zoe,Adam,Dan

Array.prototype.join                    // Similar to toString, but you can specify the separator:
let names = ["Zoe", "Adam", "Dan"]
let strNames = names.join(" and ")      // Zoe and Adam and Dan

Array.prototype.concat                  // Create a new array by concatenating existing arrays:
let nums = [1, 2, 3]
let nums2 = [4, 5, 6]
let nums3 = [7, 8, 9]
let concatArr = nums.concat(nums2, nums3)// [1, 2, 3, 4, 5, 6, 7, 8, 9]

Array.prototype.splice                  //The splice() returns an array(mutates the original array) & can be used to add new items to an array:
let arr = ["Danny", "Joe"]
arr.splice(1, 0, "Alice", "Amy")
console.log(arr)                        // ['Danny', 'Alice', 'Amy', 'Joe']

Array.prototype.slice                   //slice() slices out a piece of an array, and returns it in a new array (does not mutate the original array):
let arr = ["Danny", "Joe", "Amy"]
let slice = arr.slice(1)                // ['Joe', 'Amy']
let arr = ["Danny", "Joe", "Amy"]
let slice = arr.slice(0, 2)             // ['Danny', 'Joe']

Array.prototype.indexOf                 //Find the first index that contains a certain value (searches from left to right):

let arr = ["Danny", "Joe", "Amy", "Joe"]
let index = arr.indexOf("Joe")          // 1

Array.prototype.lastIndexOf             //Find the last index that contains a certain value (searches from right to left):

let arr = ["Danny", "Joe", "Amy", "Joe"]
let index = arr.lastIndexOf("Joe")      // 3

// ___________Higher-order array methods___________________
/*  A higher-order function is a function that accepts functions as arguments, and/or returns a function. 
   So, higher-order functions are functions that operate on other functions.
*/
Array.prototype.forEach
 
for(let i = 0; i < arr.length; i++) {...}.  //The forEach method is basically just a shorter way of writing
// It loops through the given array, and calls the given call-back function for each of the elements in the array.
// The call-back passed to the forEach() function can accept any of the three arguments:
let numbers = [1, 2, 3, 4]
numbers.forEach(n => console.log(n))
// 1
// 2
// 3
// 4
// It's better to use map if you want to return a new array with return value of each call-back run.

Array.prototype.map                          //return  new array. It does not mutate the original array.
let numbers = [1, 2, 3, 4]
// Double all numbers
let doubledNumbers = numbers.map(n => n * 2) // [2, 4, 6, 8]
// Only double numbers at odd indexes
let doubledOddIndexNumbers = numbers.map((n, i) => {
  if (i % 2 === 1) return n * 2
  else return n
}) // [1, 4, 3, 8]

Array.prototype.filter
//A good use case for filter is a search bar:
let articles = [
  { title: "PHP classes", author: "Danny Adams" },
  { title: "Python arrays", author: "Amy Sanders" },
  { title: "Arrays in PHP", author: "Danny Adams" },
]
// Lets say the user searches for all articles with PHP in the title
let PHPArticles = articles.filter(a => a.title.includes("PHP"))
// [
//   { title: 'PHP classes', author: 'Danny Adams' },
//   { title: 'Arrays in PHP', author: 'Danny Adams' },
// ];

//Another use case is filtering via size:
let cities = [
  { name: "Stokington", rivers: 3 },
  { name: "Phillydelfia", rivers: 6 },
  { name: "New Ports", rivers: 2 },
]
let moreThanTwoRivers = cities.filter(c => c.rivers > 2)
// [
//   { name: 'Stokington', rivers: 3 },
//   { name: 'Phillydelfia', rivers: 6 },
// ];

Array.prototype.reduce
let numbers = [1, 2, 3, 4]
let total = numbers.reduce((total, currentNum) => total + currentNum) // 10

Array.prototype.some           //The some method checks if some array values pass a test. It returns either true or false.
let numbers = [4, 6, 14, 16]
let isSomeGreaterThan6 = numbers.some(n => n > 6)    // true
let isSomeLessThan4 = numbers.some(n => n < 4)       // false

Array.prototype.every    //every is similar to the some method, but checks if every value in the array passes a certain test, rather than just some.

Example:
let numbers = [4, 6, 14, 16]
let isEverythingGreaterThan6 = numbers.every(n => n > 6) // false
let isEverythingLessThan20 = numbers.some(n => n < 20)   // true

Array.prototype.find             //The find method returns the first element in the array that passes a certain test.
let stock = [
  { item: "ketchup", quantity: 32 },
  { item: "mayo", quantity: 9 },
  { item: "hot sauce", quantity: 12 },
]
let mayo = stock.find(s => s.item === "mayo")      //  { item: 'mayo', quantity: 9 }

Array.prototype.findIndex        //Same as find, but returns the index instead of the value:

let stock = [
  { item: "ketchup", quantity: 32 },
  { item: "mayo", quantity: 9 },
  { item: "hot sauce", quantity: 12 },
]
let mayoIndex = stock.findIndex(s => s.item === "mayo")    //  1

Array.prototype.sort            //sort puts an array's elements in ascending order.it mutates the original array and returns it.
let names = ["Zoe", "Adam", "Dan"]
names.sort()
console.log(names)              // ['Adam', 'Dan', 'Zoe']

let numbers = [3, 1, 7, 2]
numbers.sort((a, b) => a - b)
console.log(numbers)           // [1, 2, 3, 7]

// ___________Global Functions()_________
eval();                     // executes a string as if it was script code
String(23);                 // return string from number
(23).toString();            // return string from number
Number("23");               // return number from string
decodeURI(enc);             // decode URI. Result: "my page.asp"
encodeURI(uri);             // encode URI. Result: "my%page.asp"
decodeURIComponent(enc);    // decode a URI component
encodeURIComponent(uri);    // encode a URI component
isFinite();                 // is variable a finite, legal number
isNaN();                    // is variable an illegal number
parseFloat();               // returns floating point number of string
parseInt();                 // parses a string and returns an integer

// _________Regular Expressions\n________
let a = str.search(/CheatSheet/i);
// Modifiers
/*i   perform case-insensitive matching
g   perform a global match
m   perform multiline matching*/

// _______Errors⚠__________
try {                           // block of code to try
undefinedFunction();
}
catch(err) {                    // block to handle errors
console.log(err.message);
}
// _______Throw error________
throw "My error message";    // throw a text

//_________Input validation________
let x = document.getElementById("mynum").value; // get input value
try { 
if(x == "")  throw "empty";                 // error cases
if(isNaN(x)) throw "not a number";
x = Number(x);
if(x > 10)   throw "too high";
}
catch(err) {                                    // if there's an error
document.write("Input is " + err);          // output error
console.error(err);                         // write the error in console
}
finally {
document.write("</br />Done");              // executed regardless of the try / catch result
}

// ________Error name values________
/*RangeError      A number is "out of range"
ReferenceError  An illegal reference has occurred
SyntaxError     A syntax error has occurred
TypeError       A type error has occurred
URIError        An encodeURI() error has occurred */

// _______JSONj_________
let str = '{"names":[' +                    // crate JSON object
'{"first":"Hakuna","lastN":"Matata" },' +
'{"first":"Jane","lastN":"Doe" },' +
'{"first":"Air","last":"Jordan" }]}';
obj = JSON.parse(str);                      // parse
document.write(obj.names[1].first);         // access

// ______Send__________
let myObj = { "name":"Jane", "age":18, "city":"Chicago" };  // create object
let myJSON = JSON.stringify(myObj);                         // stringify
window.location = "demo.php?x=" + myJSON;                   // send to php

// __________Storing and retrieving_____
myObj = { "name":"Jane", "age":18, "city":"Chicago" };
myJSON = JSON.stringify(myObj);                 // storing data
localStorage.setItem("testJSON", myJSON);   
text = localStorage.getItem("testJSON");        // retrieving data 
obj = JSON.parse(text);
document.write(obj.name);

// ________Promises________
function sum (a, b) {
return Promise(function (resolve, reject) { 
 setTimeout(function () {                                       // send the response after 1 second
   if (typeof a !== "number" || typeof b !== "number") {        // testing input types
	 return reject(new TypeError("Inputs must be numbers"));
   }
   resolve(a + b);
 }, 1000);
});
}
let myPromise = sum(10, 5);
myPromsise.then(function (result) {
document.write(" 10 + 5: ", result);
return sum(null, "foo");              // Invalid data and return another promise
}).then(function () {                   // Won't be called because of the error
}).catch(function (err) {               // The catch handler is called instead, after another second
console.error(err);                   // => Please provide two numbers to sum.
});

// _______States________
pending, fulfilled, rejected
// _______Properties_______
Promise.length, Promise.prototype
// _______Methods_______
Promise.all(iterable), Promise.race(iterable), Promise.reject(reason), Promise.resolve(value)

</script>