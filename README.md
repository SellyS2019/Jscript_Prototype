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
![Function_Prototype_rs](https://user-images.githubusercontent.com/48932121/64507898-3fd6cf00-d31f-11e9-9549-b97a25404259.png)

![Function_Prototype_Object](https://user-images.githubusercontent.com/48932121/64508171-0f436500-d320-11e9-9eb6-3c8569a92aae.png)

![Prototype_equal_dundeeproto](https://user-images.githubusercontent.com/48932121/64508283-6a755780-d320-11e9-89ea-258ef61956fb.png)
