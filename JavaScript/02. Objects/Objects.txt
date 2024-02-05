// Objects

Objects can be declared in two ways :-
1. Literals - Not Singleton, multiple instances of an object.
// Implementation :
const obj = {
    name : "Himanshu",                  // By default Babel treats key as string literals i.e. name as "name", age as "age"
    age : 22
}

2. Constructor - Singleton, only one copy of an object.
// Implementation
const obj = Object.create(null)

There are two ways to access keys and value inside an object :-
const obj = {
    name : "Himanshu Oli",
    age : 22,
    comitted : false
}
1. console.log(obj.name)                     // Dot notation is more concise and easier to read.
2. console.log(obj["name"])                  // Bracket notation is more versatile.

Note : One difference between dot notation and bracket notation -
const obj = {
    "full name" : "Himanshu Oli",
    age : 22,
    uid : "21BCS7367"
}
console.log(obj.full name)                 // Cannot access using dot notation
console.log(obj["full name"])              // Correct Way

const StudentDetails = {
    "First Name" : "Himanshu",
    "Last Name" : "Oli",
    age : 22,
    uid : "21BCS7367",
    "Full Name" : function () {
        return this["First Name"]+" "+this["Last Name"]
    }
}
console.log(StudentDetails["First Name"])            // Output : Himanshu
console.log(StudentDetails["Last Name"])             // Output : Oli
console.log(StudentDetails["Full Name"]())           // Output : Himanshu Oli

StudentDetails.eyeColor = "Brown"        // Add a new property in StudentDetails object.

Note : Objects are mutable. They are addressed by reference, not by value.

Note : const x = StudentDetails;  // Will not create a copy of person.
The object x is not a copy of StudentDetails. Both x and StudentDetails refers to the same object.
If we change property of x, it will also change property of StudentDetails.

**for...in Loop**








