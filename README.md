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

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
const b = {
  name: "Vivek",
  f: function () {
    var self = this;
    console.log(this.name);
    (function () {
      console.log(this.name);
      console.log(self.name);
    })();
    
  },
};
b.f();

Explanation : It will print Vivek,  then undefined or global object  because its an IIFE function it has no boundaries and vivek again because self is assigned with this (self = this) <br> this creates a reference between outer and inner function. 
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Converting array to objects 

function arrayToObject(arr){
    let obj = {};
    for(let i = 0; i<arr.length;i++){
        obj[i]=arr[i];
    }
    return obj;
}
let arr = [1,2,3,4,5];
console.log(arr);
let obj = arrayToObject(arr);
console.log(obj);

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Converting objects to arrays 
const obj = {
    name:"saqib",
    age:"23",
    gender:"male"
};

console.log(Object.keys(obj));
console.log(Object.values(obj));
console.log(Object.entries(obj));
----------------------------------------------------------------------------------------------------------------------------------------------------
