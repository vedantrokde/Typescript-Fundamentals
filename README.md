# TypeScript
TypeScript provides ‘strong typing’ that allows us to assign data type to variable and class members. These types won’t compile to JS but we will get compilation errors on assigning wrong types. It also introduces some class, interface, generic and module. These constructs makes our code cleaner, easier to read and helps us avoid nasty errors. Especially in combination with the strong typing we are really able to write high quality code and track down errors quickly. Even JS code can be written mixed with TypeScript, using ‘var’ instead of ‘let’ or using pure JS libraries.

## Variable Declaration

```
// Declaration of string 

let myString!: string;
myString!: string;
myString = '';
```

```
// this will raise an error
myString = 4
```

```
//this is assigned to type any by default then can be assigned any type of data
let myString;
```

```
// other basic types
let aString: string;
let aNumber: number;
let aBoolean: boolean;
let aArray: Array<string>;
let aAnything: any;
```

## Classes
```
class Person {
    private name: string;
    private email: string;
    private age: number;

    constructor(name: string, email: string, age: number) {
        this.name = name;
        this.email = email;
        this.age = age;
    }
    
    // getters and setters ...
}
```

```
let person = new Person('aman', 'aman@example.com', 34);
console.log("Person's Name: ", person.getName());
```

## Interface
```
interface User {
    username: string;
    password: string;
    confirmPassword?: string; // Optional property => Does not have to be implemented
}
let user: User;
user = {username: 'aman', password: 'password'}

interface CanDrive {
    accelerate(speed: number): void;
}
let car:CanDrive = {
    accelerate: function(speed: number) {
        ...
    }
};
```

## Generics
```
// there are the types that can hold or user several types. eg. Array
let numberArray: Array<number>;
numberArray = [1,2,3];
```

```
// this will generate error
numberArray = ['test'];
```

## Modules
```
export class ExportedClass{
    // this exporting makes the class a module
}
```

## RxJS map operators for ngrx effects
* mergeMap -  can be used for deleting items 
* concatMap - can be used for updating or creating items
* exhaustMap - can be used for getting some data from the server.
* switchMap - can be used for search functions.
