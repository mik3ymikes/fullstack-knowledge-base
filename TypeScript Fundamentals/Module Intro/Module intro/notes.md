#Module introduction
type script just extends javascript-what it is why would we use. Core Concepts

#what and why
Superset to Javascript.Adds static typing to Javscript
Javascript is dynamically type...takes what it can get and tries to execute
function could take strings or numbers...may not be the best and cause errors

function add(a:number, b:number){
return a+b
}
this makes it clear that should be numbers

#Installing typeScript
go to typescript and have node js installed
in the terminal with bash npm install typescript. Can now use complier. type script does not run in browser. npx tsc (javascript file) then it gets complied.
could complie code to run in old javscript

#Base Types Primitives
numbers,stings,booleans
let age:number;

age=12

let userName:string

userName="Max"

#Array and object types

let hobbies:string[]

hobbies=["sports", "cooking"]

any type is the default and not very useful

let person:{
name:string;
age:number
}

person={
name:"Max",
age:32
}

person={
isEmployee:true
}
wont work cus wrong type

let people:{
name:string;
age:number;

}[];

means I want an object in an array

#type inference

by deafult it will guestimate what is needed

let course="react"

error here cuz it was a string then changed to numb
course=1234

#UNIONS
inference isnt good if you got more than one type
let course:string | number="react is fun" //so now can use both

course=12324

#ALIASES
Base type is used instead of repating....use type keyword
type Person={
name:string,
age:number
}

this an allias...can use them on multipe items
let person:Person

person={
name:"max",
age:43
}

#diving into functions
types can be assigned if diffrent places..variables..parameters
part outside the parenthisis is what value should be//should have to edo that tho
function add(a:number, b:number):number{
return a +b
}

#generics
should lookinto it more? that thhe type put in should be the same?

function insertAtBegin<T>(array:T[], value:T){
const newArray=[value,...array]
return newArray
}

const demoArray=[1,4,5]

const updatedArray=insertAtBegin(demoArray,-1)

#Classes and typescript
Can implement classes and private properties or public
class Student{
firstName:string;
lastName:string;
age:number;
private courses:string[]

     constructor(first:string, last:string, age:number, courses:string[]){
         this.firstName=first;
         this.lastName=last;
         this.age=age;
         this.courses=courses
     }

     enrol(courseName:string){
         this.courses.push(courseName)
     }
     listCourses(){
        return this.courses.slice()
     }

/ }

const student=new Student("max", "swan", 34, ["ang"])
student.enrol("react")

console.log(student.courses)

#INterfaces
only exist in typescript and not javascript...object type defintions
interface Human{
firstName:string;
age:number;

    greet:() => void;

}

can only follow structure set
let max:Human;

max={
firstName:"max",
age:32,
greet() {
console.log("hi")
},
}

or can use implements
class Instructor implements Human{
firstName:"max";
age:32;
greet() {
console.log("hi")
}
}

interfaces could be used instead of types and can be implemented by classes
