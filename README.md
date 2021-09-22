# Hello_World

Hey y'all!

My name is Sam Marold, I am a senior at the University of Iowa. 
I'm going for a double major with a B.B.A. in Accounting and a B.B.A. in Business Analytics.
My passions include:
1. The outdoors (hiking, skiing, rafting)
2. Music (guitar, singing, producing)
3. Just about everything involving sports!

# Student Loan Problem
### Description
For this problem, I had to create a simulation for a student loan situation.
Using Python, I coded a program that takes inputs for number of years, loan amount per year, and interest rate.
Next, the program computes the total amount owed at graduation.
Finally, the user can test different monthly payment amounts to find out if they would work, as well as how many months and years it would take to pay off the loan.
### How to Run Program
Python Code

```
## Part A ##
years = float(input("Number of Years: "))
loan_amount = float(input("Loan amount per year: "))
interest = float(input("Interest rate: "))
total_owed = (0)
counter = 0
while counter < years:
    counter += 1
    total_owed = (loan_amount + total_owed)*(1+interest)
   
print("Total Owed at Graduation")
print(int(total_owed))


## Part B ##
monthly_payment = float(input("Name a monthly payment: "))

if monthly_payment > (total_owed*interest)/12:
    print("A monthly payment of $" + str(int(monthly_payment)) + " will work!")
    print("The minimum monthly payment for this loan would be 75 dollars.")
else:
        print("A monthly payment of $" + str(int(monthly_payment)) + " won't work! You'll be paying off your loans forever.")
        print("The minimum monthly payment for this loan would be 75 dollars.")
        
        
## Part C ##

month = 0
while total_owed >= 0:
    total_owed = (total_owed - monthly_payment)
    total_owed = total_owed + ((total_owed*interest)/12)
    month += 1
    
print("It will take " + str(month) + " months to pay off your student loans.")
print("It will take " + str(month/12) + " years to pay off your student loans.")
```

### Files Used [^1]
[^1]: There were no files used for this problem.
### Additional Documentation [^1]
[^1]: There is no additional documentation for this problem.
### Versioning [^1]
[^1]: There is no versioning at this time.
