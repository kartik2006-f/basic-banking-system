🏦 Basic Banking System using Java (OOP)
Welcome to the Basic Banking System! This project simulates a simple banking application using Java and Object-Oriented Programming (OOP) principles. It allows users to create accounts, deposit and withdraw money, and view their balances.

👨‍💻 Team Members
Rajnish Kumar (Team Leader) - 24SCSE1180331
Pratyush Sen - 24SCSE1180686
Kartik Saini - 24SCSE1180186
Adarsh Shukla - 24SCSE1180394
🧠 Project Overview
This Java-based console application demonstrates:

Abstraction via an abstract BankAccount class
Inheritance with SavingAccount and CurrentAccount
Encapsulation and Polymorphism for functionality
Modular design in BankingSystem class


🔁 Flow of the Program
text
Copy code

START

   ↓
   
Create Account


   ↓
   
Login

   ↓
   
Deposit ₹1000

   ↓
   
Withdraw ₹500

   ↓
   
View Current Balance

   ↓
   
Logout

   ↓
   
STOP

🗂️ Class Diagram

plaintext

Copy code

               ┌──────────────────┐
               │  BankAccount     │
               │------------------│
               │ - accountNumber  │
               │ - balance        │
               │------------------│
               │ + deposit()      │
               │ + withdraw()     │
               │ + getBalance()   │
               └────────┬─────────┘
                        │
         ┌──────────────┴──────────────┐
         │                             │
      SavingAccount               CurrentAccount   
          
         

                    ┌────────────────────┐
                    │   BankingSystem    │
                    │--------------------│
                    │ + main()           │
                    └────────────────────┘
🧾 Sample Java Code
Abstract Class BankAccount
java
Copy code
public abstract class BankAccount {
    protected String accountNumber;
    protected double balance;

    public BankAccount(String accountNumber) {
        this.accountNumber = accountNumber;
        this.balance = 0.0;
    }

    public void deposit(double amount) {
        balance += amount;
    }

    public abstract void withdraw(double amount);

    public double getBalance() {
        return balance;
    }
}
SavingAccount Class
java
Copy code
public class SavingAccount extends BankAccount {
    public SavingAccount(String accountNumber) {
        super(accountNumber);
    }

    @Override
    public void withdraw(double amount) {
        if (balance >= amount) {
            balance -= amount;
        } else {
            System.out.println("Insufficient balance!");
        }
    }
}
BankingSystem Entry Point
java
Copy code
import java.util.Scanner;

public class BankingSystem {
    public static void main(String[] args) {
        // Entry point with account creation, login, and transactions
        Scanner scanner = new Scanner(System.in);
        // Simulated logic here...
    }
}
📸 Sample Console Output
Welcome to the Basic Banking System
1. Create Account
2. Login
3. Exit

> Create Account
Enter account type (Savings/Current): Savings
Account created successfully!

> Login
Enter account number: 123456
Login successful!

> Deposit ₹1000
Deposit successful. Balance is now ₹1000.

> Withdraw ₹500
Withdrawal successful. Balance is now ₹500.

> Check Balance
Current Balance: ₹500

> Logout
Logged out successfully.
📜 License
This project is licensed for educational purposes only and should not be used for real-world banking applications.

🙏 Acknowledgements
Special thanks to all team members and mentors who supported the development of this project.

⚠️ Disclaimer: This is a basic educational project and does not include data persistence, encryption, or secure authentication.
"""
