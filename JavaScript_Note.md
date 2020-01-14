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


