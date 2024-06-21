# Welcome to Digipen!!
TODO

# Introduction to C++

## What is C++
C++ (pronounced "C plus plus") is a high-level, general-purpose programming language created by Danish computer scientist Bjarne Stroustrup. First released in 1985 as an extension of the C programming language. Source: Wikipedia.

### What is a programming language
A programming language is a vocabulary (keywords) and set of grammatical rules (syntax) for instructing a computer or computing device to perform specific tasks.

# Hello World
The first program we are going to do is the popular "Hello World!" program. Used in programming as the first program to do in any porgramming language when anyone is trying to learn it.

You can check the code in the file ```helloworld.cpp```
  
```c++
#include <iostream>

int main() {
  std::cout << "Hello World!\n";
}
```

If you press the run button you will se the result of this program. It will appear in the console. You will see that "Hello World!" is printed in the console.

Lets see all the parts of this code.

# Library
A programming library is a collection of prewritten code that programmers can use to optimize tasks. This collection of reusable code is usually targeted for specific common problems.

To use a library in our program we have to use the ```#include``` keyword.
In our Hello World program we are using the iostream library, that allow us to perform different input and output operations.

# Function (Introducion)
A function is a block code that can be used in programming. This block code is going to have:
1. header ```int main()```
2. code. The code is going to be inside the curly braces ```{ }```

In this first program we are using the main function. The main function is a special function, because it is the one used by the computer to start the program. So our program will start in he main function.

# Sentence
A sentence is a individual instruction that perform specific action.

If we check the sentence ```std::cout << "Hello World!\n";``` we see that it has 3 parts: 
1. ```std::cout``` is the function that will print in the screen. This function is included in the iostream library.
2. ```<<``` is the operator.
3. ```"Hello World!\n"``` is what we want to print.

So we are telling the computer to print in the screen the text "HelloWord".

Why are we using ```\n``` after hello word?? It is going to make a change of line. So if we want to print several lines we have to use it.

Sentences always finish with the semicolon symbol ```;```.

# Variable
A variable is a value that can change, depending on conditions or on information passed to the program.
A variable declaration has 2 parts:
1. Data type of the variable
2. Identifier of tha variable

We are going to introduce variables in our program. First we are going to introduce a number. First we have to put the data type, as it is a number the data type is going to be ```int``` that stands for integer. Then we are going to put a space and an identifier. As we are going to use this variable to store our age, we are going to use the word "age" as identifier. It is important to use meaningfull words as identifiers. This code must be included inside the function main.

```c++
#include <iostream>

int main() {
  int age;
  std::cout << "Hello World!\n";
}
```
Now we have declared a variable, but we are not using it. We are going to introduce a new sentence to store a value in that variable. To do that we are going to use the assignment operator ```=```;
```c++
#include <iostream>

int main() {
  int age = 16; // Put here your age
  std::cout << "Hello World!\n";
}
```
We have now storing the number 16 in the variable age. We are going to introduce a new sentence to print our age. At this point we now how to print text on the screen, to print a variable we just have to replace the text by the name of the variable (without using quotes).
```c++
#include <iostream>

int main() {
  int age = 16;
  std::cout << "Hello World!\n";
  std::cout << "I am " << age << " years old.\n";
}
```

It is time to run the program an check if the result is correct in the console.

We are going to introduce a new variable. We are going to use it to store a name. As a name is a different type of variable we need to use another type. In this case the type is an array of char  [], this is going to represent a serie of characters, that will make the name.

```c++
#include <iostream>

int main() {
  int age = 16;
  char name[] = "Jon"; // Notice the position of the [ ]
  std::cout << "Hello World!\n";
  std::cout << "I am " << age << " years old.\n";
}
```
Now it is time to introduce a new output sentence to show our name.
```c++
#include <iostream>

int main() {
  int age = 16;
  char name[] = "Jon";
  std::cout << "Hello World!\n";
  std::cout << "My name is " << name << " and ";
  std::cout << "I am " << age << " years old.\n";
}
```

# Function
It is time to go deeper over functions. We have used up to now the main function, now we are going to create a new function. Functions are similar to math function y = F(x), so we are going to have a piece of code that is going to receive x argument/s and return a value y. First we need to declare the function, to do that we must use the following syntax: ```return-type function_name (arguments)```.
1. return-type is the type of the value the function is going to return.
2. function_name is used to identify the function (similar to the identifier of a variable)
3. arguments are the information we pass to the function. Arguments must be declared as variables with a pair of type-identifier.

We are going to create a new function to calculate our age next year. 

```c++
int AgeNextYear(int currentAge)
{
  return currentAge + 1;
}
```
1. return_type is int, so it is going to be a number
2. function_name is AgeNextYear
3. argument currentAge type is int.
4. return is a new keyword, it is used to finish the execution of the function and return the value produced by the function.

The function will receive the current age and will return the age we will be next year.

## Function call
Now we have the main function and our new created function, but there is no relation between them. To be able to use our new function we must call it. To call the function we must provide the argument.

```c++
#include <iostream>

int AgeNextYear(int currentAge)
{
  return currentAge + 1;
}

int main() {
  int age = 16;
  char[] name = "Jon";
  std::cout << "Hello World!\n";
  std::cout << "My name is " << name << "and ";
  std::cout << "I am " << age << " years old.\n";
  std::cout << "Next year I will be " << AgeNextYear(age) << " years old\n";
}
```
This way we will call our function, pass the current age as argument and the function will return the value of the age +1 (see the code of the function).

Note that the function must be declared before the function call. That is why our function AgeNextYear is before the main function.

# Variables (new data types)
Up to now we have used int type to store numbers, but it only stores integer numbers, so we can not store fractional numbers as 1/2, or 0.5.
We are going to use a new type of variable: float

```c++
#include <iostream>

int AgeNextYear(int currentAge)
{
  return currentAge + 1;
}

int main() {
  int age = 16;
  char[] name = "Jon";
  floar height = 1.70; // put your heigth here
  std::cout << "Hello World!\n";
  std::cout << "My name is " << name << "and ";
  std::cout << "I am " << age << " years old.\n";
  std::cout << "Next year I will be " << AgeNextYear(age) << " years old\n";
}
```
Now we are going to store our heigth. Our heigth is going to be stored in meters so we need to store a fractional part, and we can not do it using a variable of type int, we will need to use a variable of type float.


```c++
#include <iostream>

int AgeNextYear(int currentAge)
{
  return currentAge + 1;
}

int main() {
  int age = 16;
  char[] name = "Jon";
  floar height = 1.70; // put your heigth here
  std::cout << "Hello World!\n";
  std::cout << "My name is " << name << "and ";
  std::cout << "I am " << age << " years old.\n";
  std::cout << "Next year I will be " << AgeNextYear(age) << " years old\n";
}
```