
<H1 ALIGN =CENTER>Exp03-Constructor</H1>

## Aim: 
To write a C# program to calculate the salary of an employee by passing the name, designation, noofexperience, basic salary and insurance amount through constructor.

## Algorithm:
### Step1:
Initialize the program with the system library
### Step2:
Define the Employee Class and set it as public
### Step3:
Define the variables
### Step4:
Write a parameterized constructor under the class Employee
### Step5:
Define a function to calculate the salary
### Step6:
Define the display() function to print the output

## Program:
```cs
using System;

namespace Exp3
{
    public class Employee
    {
        public string name, designation;
        public int bsalary, noofexp, insurance;
        public float hra, ta, grosspay;
        public Employee(string name, string designation, int bsalary, int noofexp, int insurance)
        {
            this.name = name;
            this.designation = designation;
            this.bsalary = bsalary;
            this.noofexp = noofexp;
            this.insurance = insurance;
        }
        public void salary()
        {
            hra = (20 / 100) * bsalary;
            ta = (10 / 100) * bsalary;
            grosspay = bsalary + hra + ta - insurance;
        }
        public void display()
        {
            Console.WriteLine("{0} having {1} yrs of experience, working as {2}", this.name, this.noofexp, this.designation);
            Console.WriteLine("Receives {0} as his/her salary", this.grosspay);
        }
    }
    class Program
    {
        public static void Main(string[] args)
        {
            Employee emp1 = new Employee("Vijay", "ML Engineer", 120000, 5, 20000);
            emp1.salary();
            Employee emp2 = new Employee("SK", "Data Scientist", 90000, 2, 10000);
            emp2.salary();
            emp1.display();
            emp2.display();
            Console.ReadLine();
        }
    }
}
```
## Output:

![img1](https://github.com/ragulmani936/Exp03-Constructor/assets/94881918/490b9a43-4b60-4c51-81bd-86d8d75aaeab)


## Result:
Thus, a C# program is written to calculate the salary of an employee using a constructor is implemented and the output is verified.
