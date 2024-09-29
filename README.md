# Experiment13
## Aim:-
To study and implement Constructor Overloading in C++.

## Apparatus
IDE: Visual Studio Code (VS Code)
## Theory
What is Constructor Overloading?
Constructor overloading allows a class to have more than one constructor, each with a unique parameter list. This provides flexibility in initializing an object in different ways based on the arguments passed during object creation.

### Key Concepts
1. Multiple Constructors: Constructor overloading enables multiple constructors in a class, each with a unique set of parameters. The appropriate constructor is invoked based on the arguments passed while creating an object.
2. No Return Type: Constructors do not return any value, including void. Their sole purpose is to initialize the object.
3. Default Constructor: This constructor has no parameters and initializes objects with default values. If no constructor is explicitly defined, the compiler provides a default constructor.
4. Parameterized Constructor: A constructor that takes parameters to initialize an object with specific values during its creation.
5. Copy Constructor: A constructor that creates a new object as a copy of an existing object by taking a reference to another object of the same class.

## Code:

1. 
```
// ashu yadav
// 23070123110
#include <iostream>
using namespace std;

class Room {
private:
    double length;
    double breadth;

public:
    // Default Constructor
    Room() {
        length = 9;
        breadth = 7;
    }

    // Parameterized Constructor
    Room(double l, double b) {
        length = l;
        breadth = b;
    }

    // Constructor with one parameter
    Room(double len) {
        length = len;
        breadth = 8.1;
    }

    double calculateArea() {
        return length * breadth;
    }
};

int main() {
    Room r1;             // Default constructor
    Room r2(8.6, 6.9);   // Parameterized constructor
    Room r3(9);          // Single parameter constructor
       
    cout << "Area of r1: " << r1.calculateArea() << endl;
    cout << "Area of r2: " << r2.calculateArea() << endl;
    cout << "Area of r3: " << r3.calculateArea() << endl;

    return 0;
}
```
Output:

![image](https://github.com/user-attachments/assets/a27679c0-458d-4ea2-9e06-826cd8948c85)


2. 

```
// ashu yadav
//23070123154
#include <iostream>
using namespace std;

class Fetch {
    int num;

public:
    // Default Constructor
    Fetch() {
        num = 45;
        cout << num << " 1st (Default Constructor)" << endl;
    }

    // Parameterized Constructor
    Fetch(int x) {
        num = x;
        cout << num << " 2nd (Parameterized Constructor)" << endl;
    }

    // Copy Constructor
    Fetch(const Fetch &b) {
        num = b.num;
        cout << num << " (Copy Constructor)" << endl;
    }

    void display() const {
        cout << num << endl;
    }
};

int main() {
    Fetch f1;        // Calls default constructor
    Fetch f2(25);    // Calls parameterized constructor
    Fetch f3(f1);    // Calls copy constructor

    f1.display();
    f2.display();
    f3.display();

    return 0;
}
```
Output:

![image](https://github.com/user-attachments/assets/c3a000fc-09fe-4676-a6f9-bdb81ab0f5e5)


## Conclusion:
Constructor overloading is a powerful feature in C++ that increases flexibility and simplifies the process of object creation. By utilizing overloaded constructors, we can create objects with different initialization parameters, improving the efficiency and readability of the code.
