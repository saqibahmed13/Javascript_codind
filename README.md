# Javascript codes

let x= {}, y = {name:"Ronny"},z = {name:"John"};
x[y] = {name:"Vivek"};
x[z] = {name:"Akki"};
console.log(x[y]);  // output name: Akki

Explanation: When we use objects as keys x[y]  (y is an object) it will be converted into a string x[ object Object ] since we are using twice the value will be <br>
x[z] overwrites the previous value by name : Akki. 
