# Jscript_Prototype
Lesson
PROTOTYPE

=====
Storing separate instances of function for each object results into wastage of memory

One of the ways to create objects in JavaScript is using the constructor function.

Problem with creating objects with the constructor function:
```
function Human(firstName, lastName) {
	this.firstName = firstName,
	this.lastName = lastName,
	this.fullName = function() {
		return this.firstName + " " + this.lastName;
	}
}

let person1 = new Human("Virat", "Kohli");

console.log(person1)
```

prototype property of the function is an object (prototype object) with two properties:

constructor property which points to Human function itself

__proto__ property: We will discuss this while explaining inheritance in JavaScript

```
function Human(firstName, lastName) {
	this.firstName = firstName,
	this.lastName = lastName,
	this.fullName = function() {
		return this.firstName + " " + this.lastName;
	}
}

let person1 = new Human("Selly", "Santoso")

console.log (Human.prototype)
console.log (person1._proto_)
console.log(person1.prototype)

console.log(`($(Human.prototype===person1===_proto_))`)
console.log(`(person1._proto_===person1._proto_)`)

```




