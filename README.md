# Ex04-Constructor
## Aim:
 To write a C# program to calculate the salary of an employee by passing the name, designation, noofexperience, basic salary and insurance amount through constructor.
 
 ## Algorithm:
### Step 1:
Create a class and a constructor.

### Step 2:
Get name, designation, experience, basic salary and insurance amount from the User.

### Step 3:
Call salary method in constructor to calculate salary.

### Step 4:
Call display method to display the output.

### Step 5:
Stop the program.

 ## Program:
 ```
 using System;
public class Employee
{
   public String designation;
   public String employee_name;
   public int exp;
   public int bs;
   public int insurance;
   double hra, ta, salary;

   public Employee(String employee_name, String designation, int exp, int bs, int i)
   {
       this.employee_name = employee_name;
       this.designation = designation;
       this.exp = exp;
       this.bs = bs;
       this.insurance = i;
   }
   public void sal()
   {
       hra = this.bs * 0.2;
       ta = this.bs * 0.1;
       salary = this.bs + hra + ta - this.insurance;

   }
   public void display()
   {

       Console.WriteLine("Name of the employee is {0} having {1} of experience,working as {2}.", this.employee_name, this.exp, this.designation);
       Console.WriteLine("Receives {0} of salary.", salary);

   }

}
class TestEmployee
{
   public static void Main(string[] args)
   {
       Employee e1 = new Employee("Sowmya", "MANAGER", 8, 60000, 9000);
       e1.sal();
       Employee e2 = new Employee("Jhansi", "Team Lead", 5, 50000, 3000);
       e2.sal();
       e1.display();
       e2.display();

   }
}
 ```
 ## Output:
 ![output](https://github.com/jhansi21005096/Ex04-Constructor/blob/main/output.png)

 ## Result:
Thus the C# program to calculate the salary of an employee by passing the name, designation, noofexperience, basic salary and insurance amount through constructor is executed successfully.
