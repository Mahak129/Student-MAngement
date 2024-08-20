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


