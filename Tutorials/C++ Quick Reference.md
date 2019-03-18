# C++ Quick Reference

Use this document to see short examples of the various C++ topics we have coverd. This guide is intended as a *reference*, and does not replace the need to complete each tutorial.

Topics Covered: 



1. [Variables and constants](#variables)
2. Text Input 
3. Text Output
4. Operators
5. Logical Comparison
6. If statments
7. Switch case
8. Loops
9. Functions
10. && and ||
11. [Class](#class)
12. Array
13. [Vector](#vector)

*use Cmd/Ctr + f to find a topic :D*

# Variables

### Declaring and setting variables  <a name="variables"></a>

```cpp
    int age = 25;
    std::string name = "Sam";
    float height = 1.7;
```

### Declaring shared variables

```cpp
class IAP : public AserveComs  {
public:
    
    //---------------------------------------------------------------------------------
    // SHARED VARIABLES
    int lastNote;
```
### Declaring constant variables

```cpp
    const int readOnlyNumber = 10;
    const std::string readOnlyString = "Read Only";
```
<hr>

# Printing

### Printing basic text

```cpp
  std::cout << "Some basic text with a new line \n";
```

### Printing variables

```cpp    
  std::cout << "The value of a variable " << number << "\n";
```

<hr>

# Text Input

### Setting a variable
```cpp
  int age;
  std::cin >> age;
    
  std::string name;
  std::cin >> name;
```

<hr>

# Operators

### Basic math

```cpp
  int number = 5 + 6;
  int number = 6 - 5;
  int number = 6 / 2;
  int number = 6 * 5;
  // Division with remainder
  int number = 6 % 2; 
  ```
  
### With variables
```cpp
  int a = 5;
  int b = 10;
  int c = ((a + b) * a) / b;
```
### Incrementing & decrementing

```cpp
  number = number + 10;
  number = number - 5;
  
  //shorthand
  number += 3;  
  number -= 11;
```
### Incrementing & decrementing (single values only)

```cpp
  number++; //same as number += 1
  number--; //same as number -= 1
```
### Powers

```cpp
    float number = pow(2, 5); // 2 to the power of 5
    
    float number = pow(16, 0.5); // calculate square root of 16, i.e. raise to the power of 0.5
```

<hr>

# Logical Comparisons

```cpp
    bool lessThan =         5 < 2;
    bool lessThanEqual =    5 <= 5;
    bool greaterThan =      5 > 2;
    bool greaterThanEqual = 2 >= 2;
    bool isEqual =          5 == 5;
    bool isNotEqual =       5 != 4;
```

<hr>

# Conditional statements

### if
```cpp
    int number = 5;
    
    if (number < 10) {
    // compute this code only if number is less than 10
    }
```

### if-else

```cpp
    if (number == 5) {
        // compute this code only if number equals 5
    }
    else {
        //compute this code if number is any other value
    }
```

### if-else-if
```cpp
    if (number == 5) {
        // compute this code only if number equals 5
    }
    else if (number == 10) {
        // compute this code only if number equals 10
    }
    else {
        //compute this code if number is any other value
    }
```

<hr>

# Switch

```cpp
    int day;
    switch (day) {
        case 0: // same as saying if (day == 0) 
            std::cout << "Monday \n";
            break;
        case 1: // same as saying else if (day == 1) 
            std::cout << "Tuesday \n";
            break;
        case 2:
            std::cout << "Wednesday \n";
            break;
        case 3:
            std::cout << "Thursday \n";
            break;
        case 4:
            std::cout << "Friday \n";
            break;
        case 5: // fall through case
        case 6: // same as say if (day == 5 ||| day == 6)
            std::cout << "Friday \n";
            break;
        default:
            // error handling for values that don't match
            break;
    }
```

<hr>

# Loops

### While true

```cpp
  while (true) {
    //will run forever - be carefull!
  }
```

### While loop with condition

```cpp
  int counter = 0;
  while (counter < 5) {
    //will execute 5 times
    counter++;
  }
```

### Do-while loop

```cpp
  int counter = 0;
  do {
    //will execute 5 times
    counter++;
  }
  while (counter < 5);
```

### For loop
```cpp
  for (int counter = 0; counter < 5; counter++) {
    //will execute 5 times
  }
```
### For loop reverse
```cpp
  for (int counter = 4; counter >= 0; counter--) {
    //will execute 5 times
  }
```

<hr>

# Functions

### with no arguments

```cpp
    void error (); //function declaration
```

```cpp
    void IAP::error () //function definition
    {
        std::cout << "Error!;
    }
```

### with a single argument

```cpp
    void errorCode (int code); //function declaration
```

```cpp
    void IAP::errorCode (int code) //function definition
    {
        std::cout << "Error code received" << code << "!";
    }
```

### with a single argument and single return type

```cpp
    int squareNumber (int num); //function declaration
```

```cpp
    int IAP::squareNumber (int num) //function definition
    {
        int sum = num * num;
        return num; //return num
    }
```

<hr>

# && and ||

### && (and)
```cpp
    int number = 5;
    if (number >= 0 && number <= 10) {
        // code will only execute if both conditions are true
    }
```

### || (or)

```cpp
    int number = 7;
    if (number == 7 || number == 13) {
        // code will execute if either conditions are true
    }
```


<hr> 

# Class <a name="class"></a>

### Class decleration

```cpp
class Animal {
    int numOfLegs;
    std::string type;
};
```
### Class instance

```cpp
    Animal raccoon;
```

### Setting member variables

```cpp
    raccoon.type = "mammal";
    raccoon.numOfLegs = "4";
```

### Member functions


```cpp
class Animal {
    int numOfLegs;
    std::string type;
    
    bool isDangerous ()
    {
        if (numOfLegs > 4) {
            return true;
        }
        else {
            return false;
        }
    }
};
```

<hr>

# Array

### Declaration
```cpp
    std::array<int, 5> myArray; // array with 5 integer values
```

### Setting values

```cpp
    std::array<int, 5> myArray; // array with 5 integer values

    myArray[0] = 10; //setting first element to be 10
    ...
    myArray[4] = 56; //setting last element to be 56

    myArray[5] = 65; //ERROR out of bounds

    std::cout << myArray[1]; // print second element
```
### Iteration
```cpp

    std::array<int, 5> myArray; // array with 5 integer values

    //after setting some values

    for (int i = 0; i < myArray.size(); i++) {
        std::cout << myArray[i] << "\n"; //print each element of myArray in order
    }
```

### Quick Initialisation

```cpp
    std::array<int, 3> = {0,1,2}; //need as many values in braces as there are elements
```

### C style array (avoid if possible!)

```cpp
    int simpleArray[10]; //use std::array instead if possible
```

<hr>

# Vector <a name="vector"></a>

### Declaration
```cpp
    std::vector<int> myVector; // declare vector of type int
```

### Resizing
```cpp
    myVector.resize(10); // vector has 10 elements
```

### Adding values
```cpp
    myVector.push_back(10); // will increase size by 1 then set last element to be 10
```


  