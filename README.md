# class-02.md

*Code in a Content Management System*

The tools provided in the
administration sections of these
sites usually allow you to edit
parts of the page rather than
the entire page, which means
you will rarely see the <html>,
<head>, or <body> elements.
  The advantage of this approach
is that people who do not know
how to write web pages can
add information to a website
and it is also possible to change
the presentation of something
in the template, and it will
automatically update every page
that uses that template. If you
imagine an e-commerce store
with 1,000 items for sale, just 
  
  HTML STRUCTURE
  
X HTML pages are text documents.
X HTML uses tags (characters that sit inside angled
brackets) to give the information they surround special
meaning.
X Tags are often referred to as elements.
X Tags usually come in pairs. The opening tag denotes
the start of a piece of content; the closing tag denotes
the end.
X Opening tags can carry attributes, which tell us more
about the content of that element.
X Attributes require a name and a value.
X To learn HTML you need to know what tags are
available for you to use, what they do, and where they
  
  
  [Code in a Content Management System](Duckett HTML book:)
  
  
  ● Structural markup
  
  
  
  The elements that you can use to
describe both headings and paragraphs
● Semantic markup: which provides extra information; such
as where emphasis is placed in a sentence, that something
you have written is a quotation (and who said it), the
meaning of acronyms, and so on
can go.
   Basic JavaScript
This chapter is about “Basic JavaScript,” a name I chose for a subset of JavaScript that is as concise as possible while still enabling you to be productive. When you are starting to learn JavaScript, I recommend that you program in it for a while before moving on to the rest of the language. That way, you don’t have to learn everything at once, which can be confusing.

Background
This section gives a little background on JavaScript to help you understand why it is the way it is.

JavaScript Versus ECMAScript
ECMAScript is the official name for JavaScript. A new name became necessary because there is a trademark on JavaScript (held originally by Sun, now by Oracle). At the moment, Mozilla is one of the few companies allowed to officially use the name JavaScript because it received a license long ago. For common usage, these rules apply:

JavaScript means the programming language.
ECMAScript is the name used by the language specification. Therefore, whenever referring to versions of the language, people say ECMAScript. The current version of JavaScript is ECMAScript 5; ECMAScript 6 is currently being developed.
Influences and Nature of the Language
JavaScript’s creator, Brendan Eich, had no choice but to create the language very quickly (or other, worse technologies would have been adopted by Netscape). He borrowed from several programming languages: Java (syntax, primitive values versus objects), Scheme and AWK (first-class functions), Self (prototypal inheritance), and Perl and Python (strings, arrays, and regular expressions).

JavaScript did not have exception handling until ECMAScript 3, which explains why the language so often automatically converts values and so often fails silently: it initially couldn’t throw exceptions.

On one hand, JavaScript has quirks and is missing quite a bit of functionality (block-scoped variables, modules, support for subclassing, etc.). On the other hand, it has several powerful features that allow you to work around these problems. In other languages, you learn language features. In JavaScript, you often learn patterns instead.

Given its influences, it is no surprise that JavaScript enables a programming style that is a mixture of functional programming (higher-order functions; built-in map, reduce, etc.) and object-oriented programming (objects, inheritance).

Syntax
This section explains basic syntactic principles of JavaScript.

An Overview of the Syntax
A few examples of syntax:

// Two slashes start single-line comments

var x;  // declaring a variable

x = 3 + y;  // assigning a value to the variable `x`

foo(x, y);  // calling function `foo` with parameters `x` and `y`
obj.bar(3);  // calling method `bar` of object `obj`

// A conditional statement
if (x === 0) {  // Is `x` equal to zero?
    x = 123;
}

// Defining function `baz` with parameters `a` and `b`
function baz(a, b) {
    return a + b;
}
Note the two different uses of the equals sign:

A single equals sign (=) is used to assign a value to a variable.
A triple equals sign (===) is used to compare two values (see Equality Operators).
Statements Versus Expressions
To understand JavaScript’s syntax, you should know that it has two major syntactic categories: statements and expressions:

Statements “do things.” A program is a sequence of statements. Here is an example of a statement, which declares (creates) a variable foo:

var foo;
Expressions produce values. They are function arguments, the right side of an assignment, etc. Here’s an example of an expression:

3 * 7
The distinction between statements and expressions is best illustrated by the fact that JavaScript has two different ways to do if-then-else—either as a statement:

var x;
if (y >= 0) {
    x = y;
} else {
    x = -y;
}
or as an expression:

var x = y >= 0 ? y : -y;
You can use the latter as a function argument (but not the former):

myFunction(y >= 0 ? y : -y)
Finally, wherever JavaScript expects a statement, you can also use an expression; for example:

foo(7, 1);
The whole line is a statement (a so-called expression statement), but the function call foo(7, 1) is an expression.

Semicolons
Semicolons are optional in JavaScript. However, I recommend always including them, because otherwise JavaScript can guess wrong about the end of a statement. The details are explained in Automatic Semicolon Insertion.

Semicolons terminate statements, but not blocks. There is one case where you will see a semicolon after a block: a function expression is an expression that ends with a block. If such an expression comes last in a statement, it is followed by a semicolon:

// Pattern: var _ = ___;
var x = 3 * 7;
var f = function () { };  // function expr. inside var decl.
Comments
JavaScript has two kinds of comments: single-line comments and multiline comments. Single-line comments start with // and are terminated by the end of the line:

x++; // single-line comment
Multiline comments are delimited by /* and */:

/* This is
   a multiline
   comment.
 */
Variables and Assignment
Variables in JavaScript are declared before they are used:

var foo;  // declare variable `foo`
Assignment
You can declare a variable and assign a value at the same time:

var foo = 6;
You can also assign a value to an existing variable:

foo = 4;  // change variable `foo`
Compound Assignment Operators
There are compound assignment operators such as +=. The following two assignments are equivalent:

x += 1;
x = x + 1;
Identifiers and Variable Names
Identifiers are names that play various syntactic roles in JavaScript. For example, the name of a variable is an identifier. Identifiers are case sensitive.

Roughly, the first character of an identifier can be any Unicode letter, a dollar sign ($), or an underscore (_). Subsequent characters can additionally be any Unicode digit. Thus, the following are all legal identifiers:

arg0
_tmp
$elem
π
 [Structural markup:](http://speakingjs.com/es5/ch01.html)
  
  
  
  
  
  
  
  
  
  ### Decision Making and Loops in C Programming


A normal program is not a sequential execution of expressions or statements one after the other. It will have certain conditions to be checked or it will have certain number of iterations. When we check for certain conditions to execute further then it called as decision statements. If the condition in decision statements are true then one set of instructions are executed, if false then another set of instructions are executed. This kind of decision is cannot be done using conditional operator. That will be mainly used to return single line of action / result. When we have to perform series of operation, we use IF conditions.

When we have to execute particular set of instructions multiple times or known number of times (iterations), then we use FOR loops or DO/WHILE loops.



Details about all these are discussed below:

Table of Contents	
If… Else Statements
For Loops
While and Do/While Loops
The general syntax for while and do/while loops are given below :
If… Else Statements
These are the decision making statements.  It is used for checking certain condition to decide which block of code to be executed. The general syntax for if..else statement is as follows:

if (condition / s){
    expressions / statements;
} else {
    expressions / statements;
}

if (condition / s){
  expressions / statements;
} else if {
  expressions / statements;
} else {
  expressions / statements;
}

The flow of code for If condition is as shown below. It verifies the condition first. If it returns TRUE value, then it continues to execute the set of expressions/statements within it, else it jumps to execute other set of expressions/statements.




If statement can take different forms. We can have single if condition, without else part. This is used when we have only set of statements to be executed when the condition is true and there is no statement for false conditions. i.e.;

if (condition / s){
  expressions / statements;
}

Eg :
if (intDivisor == 0) {
  printf ("Warning!: Divisor is Zero!!\n Please re-enter the divisor :");
  scanf ("%d", &intDivisor);
}

intResult=intDividend / intDivisor;
In above case it checks for the divisor and warns if it is zero and asks for re-entering the number. Otherwise it proceeds with normal execution of program by dividing the numbers.

If statement can have expressions to be executed when the condition is false. Those expressions are added in the else part of the ‘if’ statement.

if (condition / s) {
  expressions / statements;
} else {
  expressions / statements;
}

eg :
if (intVal >= 0)
  printf ("You entered a Positive Number!");
else
  printf ("You entered a Negative Number!");

Here it checks for the number is positive or negative and displays the message accordingly. Here we can note that we have not used curly brackets. This is because we have only one statement to be executed within if and else statements. If we have more than one expression / statements to be executed, then we need to include within curly brackets. These curly braces indicate that they are one set of expression, which needs to be executed as part of condition.
We can have if statement within another if statement, i.e.; we can have nested if statements.
e.g.: –

if (intVal >= 0)
  if (intVal == 0)
    printf ("You entered a Zero!");
  else
    printf ("You entered a Positive Number!");
else
  printf ("You entered a Negative Number!");

Here it first checks for the positive number and then within it, again checks for the zero and non-zero numbers. This kind of nesting need not be in if part alone, but can also be on else part too.
if (intVal < 0)
    printf ("You entered a Negative Number!");
else
    if (intVal == 0)
        printf ("You entered a Zero!");
    else
        printf ("You entered a Positive Number!");

This kind if nesting may look little complicated. We can make this little better by combining the else and nested if together like below :
if (intVal < 0)
  printf ("You entered a Negative Number!");
else if (intVal == 0)
  printf ("You entered a Zero!");
else
  printf ("You entered a Positive Number!");

Now this gives better understanding of the code. We can write the code in any of the above methods, depending on the requirement.
For Loops
Suppose we have to enter name a student into the program. What will we do is, we will write a message to enter the name and enter the name from keyboard while executing. Suppose we have to enter 15 such student names. What will we do now? Will we be writing scanf for 15 times? Imagine if the number of students is even more? Can we go writing scanf for so many times? What if we miss the count in between? This will result in wrong result as well as confusion to the developer / user. It simply increases the code length too.

Here the process / task are same for all the 15 or more number of students. We have to enter the names 15 times from the keyboard. The command to do this is scanf, irrespective of the number of times. That means, it’s a repetition of executing the statement scanf. Hence we can have some loop, which executes this scanf for the known number of times – here 15 or more depending on the number of students to be entered.

This kind of iteration to execute same set of expression/ statements is done by using FOR loops. This for loop can be used when we know the number of iterations or till it satisfies certain conditions. The general syntax for ‘For’ loop is given below :

for (intial_value; condition; increment_factor) {
    statement/s;
  }

Here, initial_value sets the initial value for the iteration. It can be declared and initialized within for loop itself – that is while we are setting initial value inside the ‘for’ loop. This is the initial step to be executed within for loop and is executed only once. It indicates from where the execution should begin. This can be left blank, if it is initialized outside the loop or no need to have any initial value. It is then followed by semicolon to indicate the end of initial value.
Next is the conditional check for the iteration. This is responsible for checking the condition and iterating the statements within the ‘for’ loop – body of loop. If the condition is TRUE, then it executes the steps within it. If the condition fails or return FALSE, then it exits the loop and proceeds with next set of statements outside the loop. There can be one or more conditions here, joined together by using logical operators. Conditions can be any expression or statement using any of the operators.  This condition is repeatedly checked for each iterations of the loop. This is followed by semicolon to indicate the end of it.


Next is the increment factor which is used to increment the loop counter. This increases/decreases the iterations in the loop.

The flow chart for the execution of the for loop is shown below :




Let us consider an example to understand how for loops work. Consider a program to display first 15 natural numbers on the screen.

#include  
void main () {
  int intNum; 
  printf ("\n First 15 natural numbers are: \n");
  for (intNum = 0; intNum < 15; intNum++) {
    printf ("%d  ", intNum);
  }
}


In the above program, for loop initializes the value for intNum as intNum = 0. When the loop begins, it considers this initial value and checks for the condition – intNum<15, which returns TRUE. Hence executes the printf statement within it for intNum = 0. Once it is done, it increments the value of intNum by 1. Now it does not consider intNum = 0 anymore. This value is considered only once at the beginning. It checks for the n=incremented value is less than 15 or not. If yes, it continues to print the value and increments intNum. This process will go on till intNum = 15. When intNum = 15, it checks for the condition intNum
  
  * [ Decision Making and Loops in C Programming]( https://www.tutorialcup.com/cprogramming/decision-making-and-loops.htm)
