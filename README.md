# Student-MAngement

public partial class Student
{

    int studentID;
    

    string name;
    int age;
    int[] arr = new int[5];
    public Student(int studentID, string name,int age, int[]arr)
    {
        this.studentID = studentID;
        this.name = name;
        this.age = age;
        this.arr[5] = arr[5];

    }
    public void DisplayStudentInfo()
    {

    }
    public void calAvg()
    {

    }
    public void addStudentt() { }
}

public class program
{
    public static void main(String[] args)
    {

        try
        {
            int command ;
            do
            {
                Console.WriteLine("*************************Student Manangement Console Application*****************");
                Console.WriteLine("Select option");
                Console.WriteLine("1 Add Student");
                Console.WriteLine("2 Display Student Information");
                Console.WriteLine("3 Search by ID");
                Console.WriteLine("4 Get sorted student List");
                Console.WriteLine("5 Exit");

                command = int.Parse(Console.ReadLine());

                switch (command)
                {
                    case 1:
                        Console.WriteLine("Add Student Interface");

                        break;

                    case 2:
                        Console.WriteLine("Add Student Interface");
                        break;

                    case 3:
                        Console.WriteLine("Add Student Interface");
                        break;

                    case 4:
                        Console.WriteLine("Add Student Interface");
                        break;
                    case 5:
                        Console.WriteLine("Exit");
                        break;
                }
            } while (command!=5);
        
        
        }
        catch
        {

        }

    }
}














//using namespace;
using System;

public class Program()
{

    public static void checkBalance(double balance)
    {
        Console.WriteLine("your balance is = " + balance);
    }
    public static void withdrawMoney(ref double balance)
    {
        //balance += deposite;
        Console.WriteLine("enter amount to withdraw");
        double num1 = int.Parse(Console.ReadLine());
        if (num1 <= 0)
        {
            Console.WriteLine("please enter amount greater than 0 ");
        }
        else
        {
            if (balance >= num1)
            {
                balance -= num1;
                Console.WriteLine("Money Withdraw = " + num1);
            }
            else
            {
                Console.WriteLine("Insufficient Balance");
            }
        }
        
    }

    public static void depositMoney(ref double balance)
    {
        Console.WriteLine("enter amount to deposite");
        double num2 = int.Parse(Console.ReadLine());
        if (num2 <= 0)
        {
            Console.WriteLine("please enter amount greater than 0 ");
        }
        else
        {
            balance += num2;
            Console.WriteLine("money deposited = " + num2);
        }
      

    }
    public static void Main(String[] args)
    {

        double balance = 5000;



        Console.WriteLine("Enter your 4 digit pin");
        int pin = int.Parse(Console.ReadLine());
        //Bank obj1 = new Bank(deposite, withdraw);


        if (pin != 1234)
        {
            Console.WriteLine("Enter valid PIN");
        }
        else
        {
            int command;
            do
            {

                Console.WriteLine("\nEnter a command ");

                Console.WriteLine("***********************Welcome to the ATM*******************");
                Console.WriteLine("1 Check Balance");
                Console.WriteLine("2 Withdraw Money");
                Console.WriteLine("3 Deposite Money");
                Console.WriteLine("4 Exit");
                command = int.Parse(Console.ReadLine());

                switch (command)
                {
                    case 1:
                        {
                            Console.WriteLine("Balance Check interface");
                            checkBalance(balance);
                            break;
                        }
                    case 2:
                        {
                            Console.WriteLine("Withdraw Money interface");

                            withdrawMoney(ref balance);
                            break;
                        }
                    case 3:
                        {
                            Console.WriteLine("Deposit Money interface");
                            depositMoney(ref balance);
                            break;
                        }
                    case 4:
                        {
                            Console.WriteLine("Exit");
                            break;
                        }
                    default:
                        Console.WriteLine("Invalid command. Please try again.");
                        break;
                }

            }
            while (command != 4);







        }
    }
}


21August2024





using System;
using System.Diagnostics;
using System.Globalization;
using System.Xml.Linq;

public partial class Student
{

    int studentID;
    string name;
    int age;
    int[] arr = new int[3];
    public void AddStudent()
    {
        Console.WriteLine("Write Student ID");
        studentID = int.Parse(Console.ReadLine());
        Console.WriteLine("Write Student name");
        name = Console.ReadLine();
        Console.WriteLine("Enter student age");
        age = int.Parse(Console.ReadLine());
        Console.WriteLine("Enter score of subject Maths,English,Hindi");
        for(int i = 0; i < arr.Length; i++)
        {
            arr[i] = int.Parse(Console.ReadLine());
        }

       Console.WriteLine(" score of subject Maths,English,Hindi");
        for (int i = 0; i < arr.Length; i++)
        {
            Console.WriteLine(arr[i]);
        }
    }


  
    
    public void DisplayStudentInfo(List<Student> std)
    {

        Console.WriteLine("List of students:");
        foreach (var student in std)
        {
            Console.WriteLine($"Name = {student.name}, Age = {student.age}, StudentID = {student.studentID}");
        }
    }
    public void calAvg()
    {
        Console.WriteLine(" average of subject Maths,English,Hindi");
        int total = 0;
        for (int i = 0; i < arr.Length; i++)
        {
            total += arr[i];
        }
        Console.WriteLine(" average = "+total/3f);
    }
    public void SearchByID(List<Student> std)
    {
        Console.WriteLine("Enter Student ID to Search");
        int id = int.Parse(Console.ReadLine());   
        //Console.Write(std.Contains(id)); //not working
    }
    public void getSortedList(List<Student> std)
    {
        std.Sort();
        foreach(var sorted in std)
        {
            Console.WriteLine(sorted);
        }
    }
    public void AnalyseStudent(List<Student> std)
    {
        //total no of student
        Console.WriteLine("Total no of Student are: "+ std.Count);

        //longest shortest name


        //most common starting letter of names


    }
    public void removeStudent(List<Student> std)
    {

    }

}

public class program
{
    public static void Main(String[] args)
    {
        List<Student> std= new List<Student>();
        Student obj1 = new Student();

        try
        {
            int command;
            do
            {
                Console.WriteLine("*************************Student Manangement Console Application*****************");
                Console.WriteLine("Select option");
                Console.WriteLine("1 Add Student");
                Console.WriteLine("2 Display Student Information");
                Console.WriteLine("3 Search by ID");
                Console.WriteLine("4 Get sorted student List");
                Console.WriteLine("5 Analyze Student");
                Console.WriteLine("6 Remove Student");
                Console.WriteLine("7 Exit");

                command = int.Parse(Console.ReadLine());

                switch (command)
                {
                    case 1:
                        Console.WriteLine("Add Student Interface");
                       
                      
                        obj1.AddStudent();
                        std.Add(obj1);

                        Console.WriteLine("Student added successfully.\n");

                        break;

                    case 2:
                        Console.WriteLine("DisplayStudentInfo Interface");
                        obj1.DisplayStudentInfo(std);

                        break;

                    case 3:
                        Console.WriteLine("Search student by ID Interface");
                        obj1.SearchByID(std);
                        break;

                    case 4:
                        Console.WriteLine("Get Sorted List ");
                        obj1.getSortedList(std);
                        break;
                    case 5:
                        Console.WriteLine("Anaylse Student");
                        obj1.AnalyseStudent(std);
                        break;
                    case 6:
                        Console.WriteLine("Remove Student");
                        obj1.removeStudent(std);
                        break;
                    case 7:
                        Console.WriteLine("Exit");
                        
                        break;
                }
            } while (command != 6);


        }
        catch
        {

        }

    }
}
















6🈺



You are working as a database administrator for a small e-commerce company. The company has a SQL Server database that stores information about customers, products, orders, and order details. Your task is to optimize the database, create necessary views, and write queries to analyze the data. 

Task 1: Database Schema 

Create the Database and Tables: Create a database named ECommerceDB. Within this database, create the following tables: 

Customers: 

CustomerID (INT, Primary Key, Identity) 

FirstName (VARCHAR(50)) 

LastName (VARCHAR(50)) 

Email (VARCHAR(100)) 

Phone (VARCHAR(15)) 

Address (VARCHAR(255)) 

Products: 

ProductID (INT, Primary Key, Identity) 

ProductName (VARCHAR(100)) 

Price (DECIMAL(10, 2)) 

StockQuantity (INT) 

Orders: 

OrderID (INT, Primary Key, Identity) 

CustomerID (INT, Foreign Key references Customers(CustomerID)) 

OrderDate (DATETIME) 

OrderDetails: 

OrderDetailID (INT, Primary Key, Identity) 

OrderID (INT, Foreign Key references Orders(OrderID)) 

ProductID (INT, Foreign Key references Products(ProductID)) 

Quantity (INT) 

UnitPrice (DECIMAL(10, 2)) 

Insert Sample Data: Insert sample data into each of the tables. Ensure there is enough data to test various queries and views. You can create 5-10 records for each table. 

Task 2: Indexing 

Create Indexes: Create the following indexes to optimize query performance: 

A non-clustered index on the Email column of the Customers table. 

A non-clustered index on the ProductName column of the Products table. 

A composite index on the OrderID and ProductID columns of the OrderDetails table. 

Explain why you chose these columns for indexing and how it impacts query performance. 

Task 3: Views 

Create Views: Create the following views: 

CustomerOrderSummary: A view that combines customer information and their order details. Include CustomerID, FirstName, LastName, OrderID, and OrderDate. 

ProductSalesSummary: A view that provides a summary of product sales. Include ProductID, ProductName, TotalQuantitySold, and TotalRevenue. Calculate TotalQuantitySold and TotalRevenue based on OrderDetails. 

CustomerOrderDetails: A view that combines customer information with their order details and the products they purchased. Include CustomerID, FirstName, LastName, OrderID, ProductName, Quantity, and UnitPrice. 

Query the Views: Write queries to retrieve: 

The total revenue generated by each product. 

The most recent order placed by each customer. 

The top 5 customers who have placed the most orders. 

Task 4: Joins 

Write Queries Using Joins: Write SQL queries to answer the following questions: 

List all products along with their categories and the number of orders they have been included in. 

Retrieve the full order details including customer information and the products ordered. 

Find customers who have purchased a product priced over $100, and include their contact details. 
