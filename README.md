# Javascript codes

let x= {}, y = {name:"Ronny"},z = {name:"John"};
x[y] = {name:"Vivek"};
x[z] = {name:"Akki"};
console.log(x[y]);  // output name: Akki

Explanation: When we use objects as keys x[y]  (y is an object) it will be converted into a string x[ object Object ] since we are using twice the value will be <br>
x[z] overwrites the previous value by name : Akki. 

----------------------------------------------------------------------------------------------------------------------------------------------------------------
 const a = function(){
    console.log(this);
    const b = {
      func1: function(){
        console.log(this);
      }  
    }
    const c = {
      func2: ()=>{
        console.log(this);
      }
    }
    b.func1();
    c.func2();
  } 
  a();    // global/ window object , b , global/ window object 

explanation :  here a() is called it will print global object and b.func() is called it will print b and c.func2() is called since its an arrow function it doesnot have <br>
any object it will inhereit from parent class that is a function. 
