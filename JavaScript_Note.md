**Comments** 
> Inline comments // for inline comments \

> Multi-line comments  /* [your code here] */  

**Data Types: undefined, null, boolean, string, symbol, number, object** 

There are three ways to define variable:

> var myName = 'Thalia'; // This variable can be used anywhere in you script \
> myName = 'Hung'; 

> let myName = 'Thalia'; // This will only be used in the scope where you defined it 

> const pi = 3.14; // This variable will never be changed 

Example:
> var a; // Here you declare a variable \
> var b = 2; // Here you assign a variable \
> console.log(a) // a is null 
>
> a = 7; \
> b = a; // Here you assign the cotents of a to b
>
> console.log(a)  // a is 7

**String**: String can be defined using single or double quotes. \
When you string contain the quote symbol, use scape indicator back slash in front of the quote \
> var myStr = "I am \"double quoted\" string insides \"double quotes\""  \
Or, use single quote in the outer most side of the string \
> var myStr = 'I am \"double quoted\" string insides \"double quotes\"'

Other scaping methods:
> \' : single quote \
> \" : double quote \
> \\ : backslash \
> \n : newline \
> \r : cattiage return \
> \t : tab \
> \b : backspace \
> \f : form feed

Example
> var myStr = "FirstLine\n\t\\SecondLine\nThirdLine"

String concatenation use + sign
> var myName = 'Thalia ' + 'Wang' \
> var myStr = 'This is the first sentence' \
> myStr += 'This is the second sentence.'

Find the name of the string
> var lastNameLength = 0 \
> var lastName = 'Lovelace' \
> lastNameLength = lastName.length

Data slicing for string (the first index will be 0)
> var firstLetterOfLastName = '' \
> var lastLetterOfLastName = '' \
> firstLetterOfLastName = lastName[0] \
> lastLetterOfLastName = lastName[lastName.length - 1]

String in javascript is inmutable (order of letter can't be altered after defined)
> var myStr = 'Jello World' \
> myStr[0] = 'H'  // This will throw an error \
Instead, we have to do \
> myStr ='Hello World'

Variable name and function name are **case sensitive** in JavaScript

**Numerical Variable**

> var myVar = 87; \
> myVar++; // Same with myVar = myVar + 1 \
> myVar--; // Same with myVar = myVar - 1 \
> myVar += 10; // Same with myVar = myVar + 10 <br>
> myVar -= 10; // Same with myVar = myVar - 10 \
> myVar *= 5; // Same with myVar = myVar * 5 \
> myVar /= 5; // Same with myVar = myVar/5 \

> var myDecimal = 0.009; // Decimal number calculation

Find reminder of devision (find even or odd number)
> var remainder = 11 % 3;

**Array**
Store several pieces of information in one array (items don't have to be the same data type)
> var ourArray = ["John", 23]

Nested Array
> var ourArray = [["the universe", 42], ["everything", 101010]]

Access data using index in array, and modify them

> var ourArray = [50, 60, 70] \
> var ourData = ourArray[0] \
> console.log(ourData) // this is 50 \
> ourArray[0] = 45 // reassign the first value of the array \
> console.log(ourArray) // this gonna give [45, 60, 70]

Access multi-dimensional array using index
> var myArray = [[1,2,3], [4,5,6], [7,8,9], [10,11,12]]; \
> var myData = myArray[2][1]; \
> console.log(myData); // this is 8

Manipulate array using push() function
> var myArray = [["John", 23], ["cat", 2]]; \
> myArray.push(["dog", 3]); \
> // myArray is now [["John", 23], ["cat", 2], ["dog", 3]]

Manipulate array using pop() function
> var ourArray = [1,2,3] \
> var removedFromOurArray = ourArray.pop() // This gonna remove the last item from the array  \
> // removedFromOurArray now equals 3, and ourArray now equals [1,2]  

Manipulate array using shift(), unshift() function
> var ourArray = ["Stimpson", "J", ["cat"]] \
> var removedFromOurArray = ourArray.shift() // This gonna remove the first item from the array  \
> // removedFromOurArray now equals "Stimpson", and ourArray now equals ["J", ["cat"]] 

> var ourArray = ["Stimpson", "J", "cat"]; \
> ourArray.shift(); // ourArray now equals ["J", "cat"] \
> ourArray.unshift("Happy"); // ourArray now equals ["Happy", "J", "cat"] 

**Reusable code using functions**

> function name_of_your_function(){ \
>   console.log("Heyya, World"); \
> } \
> name_of_your_function();

Global scope and functions
> var myGlobal = 10; // this is a global variable\ 
>
> function fun1(){ \
>  oopsGlobal = 5; // without a var keyword, this will become a **global** variable automatically \
>  }
>
> function fun2(){ \
>   var ourpur = ""; \
>   if (typeof myGlobal != "undefined"){ \
>      output += "myGlobal: " + myGlobal; \
>    } \
>   if (typeof oopsGlobal != "undefined"){ \
>      output += "oopsGlobal: " + oopsGlobal; \
>    } \
>   console.log(output); \
>   }  
> fun1()
> fun2()

Local scope and functions (only available inside the function)
> function myLocalScope(){ \
>   var myVar = 4; \
>   console.log(myVar); \
> } \
>
> myLocalScope(); \
> console.log(myVar); // This gonna throw an error: myVar is not defined

It's possible to have global and local variable having the same name

> var outerWear = "T-Shirt"; // This is a global variable \
> 
> function myOutfit(){ \
>   var outerWear = "sweater"; // This is a local variable  \
>   return outerWear;  \
> } \
>
> console.log(myOutfit()); // This is sweater  \
> console.log(outerWear); // This is T-Shirt

Understanding Undefined value returned from a function (a function doesn't have to have a return statement)
> var sum = 0 \
> function addThree(){ \
>   aum += 3  \
> }
So if we log it out, it will be undefined/NULL

> function nextInLine(arr, item){ \
>  arr.push(item);   // push add an item at the end of array \
>  return arr.shift(); // shift remove the first item and return the first item \
>  } \
> var testArr = [1,2,3,4,5]; \
> console.log("Before: " + testArr) // This gonna give you [1,2,3,4,5] \
> console.log(nextInLine(testArr, 6)) // 1 \
> console.log("After: " + testArr) // [2,3,4,5,6] \
  
Boolean variable
> function ourTrueOrFalse(isItTrue){ \
>   if (isItTrue){ \
>     return "Yes,it's true" \
>   } \
>   return "No, it's false" \
>  } \
> ourTrueOrFalse(false) \
> ourTrueOrFalse(true)

Check for equality: The double equal sign will convert the data to same data type, but triple equal sign will not

> 3==3  true \
> 3===3 true \
> 3=="3" true \
> 3==="3" false 

!= means not equal to. Similarly, !== (strict inequality operator) will not convert data types

Logical and && /or ||
> if (val <= 50 && val >=25){ \
>    return '20 to 50' \
> } else if (val <= 90 && val >=60){ \
>    return '60 to 90' \
> } else { \
>    return 'No' \
>}

**Switch statement**
> function switchOfStuff(val){ \
> var answer = ''  \
> switch(val){  \
> case 'a': // this is checking if val == 1  \
> answer = 'alpha';  \
> break;  \
> case 'b': // this is checking if val == 2  \
> answer = 'beta';  \
> break;  \
> case 'c':  \
> answer = 'gamma'  \
> break;  \
> default: \
> answer = 'stuff'; \
> break; \
> }  \
> return answer;
> }

Test for several numbers
> function switchOfStuff(val){ \
> var answer = ''  \
> switch(val){  \
> case 1: \
> case 2: \
> case 3:  \
> answer = 'Low'  \
> break;  \
> case 4:
> case 5:
> case 6:
> answer = 'Mid'; \
> break; \
> }  \
> return answer;

**JavaScript Objects**
> var ourDog = { \ 
> "name": "Camper", // Property: value (any datatype) \
> "legs":4, \
> "tails":1, \
> "friends":["everything!"]}; \
> }

Access property of an object
> ourDog.name \
> ourDog["name"] // If there is a space in the name of the property of the object

Updating object properties
> ourDog.name = "Happy Camper"; \
> console.log(ourDog.name); //This will be "Happy Camper"

Add new properties to an object
> ourDog.bark = "bow-wow"; \
> ourDog["bark"] = "bow-wow";

Delete properties from object
> delete ourDog.bark;

Check whether an object has a certain property

> var myObj = { \
> gift: 'pony', \
> pet: 'kitten',  \
> bed: 'sleigh'}

> function checkObj(checkProp){ \
>  if (myObj.hasOwnProperty(checkProp)){  \
>    return myObj[checkProp];  \
>    } else {  \
>    return "not found"  \
>  }  \
> }
