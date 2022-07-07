# FINTECH-Bootcamp MY VERY FIRST CHALLENGE!! (no coding experience!)

## Module 1 Challenge: Loan Analyzer

### Challenge Goal 
========================================================================================
Purpose is to learn how to write codes.
Apply the what I have learned in creating variables, conditions, functions and loops.


### Writing codes (examples)
========================================================================================

Part 1: Automate the Calculations. 

    1.a Using the following data, write a code to count the number of loans.
    Data: loan_costs = [500, 600, 200, 1000, 450]
    Code: 
    number_of_loans = len(loan_costs)
    Note: Use len function to count the number of loans.

    1.b Print the number of loans.
    Code: 
    print(number_of_loans)
    Answer: 5
    
    1.c Sum the loans and print results.
    Code: 
    total_loans = sum(loan_costs)
    print(total_loans)
    #answer: 2750
    
    1.d Average the loans and print resuls.
    Code: 
    average_loans = total_loans / number_of_loans
    print(average_loans)
    #answer: 550

Part 2: Analyze Loan Data.

    Given the following loan data, you will need to calculate the present value for the loan
    loan = {
        "loan_price": 500,
        "remaining_months": 9,
        "repayment_interval": "bullet",
        "future_value": 1000,
    }

    2.a Using get function, extract the future value and remaining months on the loan and print each variable.
    Code: 
    print(loan.get("future_value"))
    print(loan.get("remaining_months"))
    #answer: 1000
    #answer: 9
    
    2.b Calculate present value.
    Code:
    present_value = loan.get("future_value") / (1 + (0.2/12)) ** loan.get("remaining_months")
    print(present_value)
    #answer: 861.7727126032183
    Note: Formula of present value: Present Value = Future Value / (1 + Discount_Rate/12) ** remaining_months

    2.c If Present Value represents what the loan is really worth, does it make sense to buy the loan at its cost?
    Write a conditional statement (an if-else statement) to decide if the present value represents the loan's fair value.
    If the present value of the loan is greater than or equal to the cost, then print a message that says the loan is worth at least the cost to buy it.
    Else, the present value of the loan is less than the loan cost, then print a message that says that the loan is too expensive and not worth the price.
    Code: 
    if present_value >= loan.get("loan_price"):
        print("The loan is worth at least the cost to buy it.")
    else:
        print("The loan is too expensive and not worth the price.")
    #answer: The loan is worth at least the cost to buy it.
      
Part 3: Perform Financial Calculations.

    Given the following loan data, you will need to calculate the present value for the loan
    new_loan = {
        "loan_price": 800,
        "remaining_months": 12,
        "repayment_interval": "bullet",
        "future_value": 1000,
    }

# @TODO: Define a new function that will be used to calculate present value.
#    This function should include parameters for `future_value`, `remaining_months`, and the `annual_discount_rate`
#    The function should return the `present_value` for the loan.
# YOUR CODE HERE!


# @TODO: Use the function to calculate the present value of the new loan given below.
#    Use an `annual_discount_rate` of 0.2 for this new loan calculation.
# YOUR CODE HERE!
print(f"The present value of the loan is: {present_value}")


"""Part 4: Conditionally filter lists of loans.

In this section, you will use a loop to iterate through a series of loans and select only the inexpensive loans.

1. Create a new, empty list called `inexpensive_loans`.
2. Use a for loop to select each loan from a list of loans.
    a. Inside the for loop, write an if-statement to determine if the loan_price is less than or equal to 500
    b. If the loan_price is less than or equal to 500 then append that loan to the `inexpensive_loans` list.
3. Print the list of inexpensive_loans.
"""

loans = [
    {
        "loan_price": 700,
        "remaining_months": 9,
        "repayment_interval": "monthly",
        "future_value": 1000,
    },
    {
        "loan_price": 500,
        "remaining_months": 13,
        "repayment_interval": "bullet",
        "future_value": 1000,
    },
    {
        "loan_price": 200,
        "remaining_months": 16,
        "repayment_interval": "bullet",
        "future_value": 1000,
    },
    {
        "loan_price": 900,
        "remaining_months": 16,
        "repayment_interval": "bullet",
        "future_value": 1000,
    },
]

# @TODO: Create an empty list called `inexpensive_loans`
# YOUR CODE HERE!

# @TODO: Loop through all the loans and append any that cost $500 or less to the `inexpensive_loans` list
# YOUR CODE HERE!

# @TODO: Print the `inexpensive_loans` list
# YOUR CODE HERE!


"""Part 5: Save the results.

Output this list of inexpensive loans to a csv file
    1. Use `with open` to open a new CSV file.
        a. Create a `csvwriter` using the `csv` library.
        b. Use the new csvwriter to write the header variable as the first row.
        c. Use a for loop to iterate through each loan in `inexpensive_loans`.
            i. Use the csvwriter to write the `loan.values()` to a row in the CSV file.

    Hint: Refer to the official documentation for the csv library.
    https://docs.python.org/3/library/csv.html#writer-objects

"""

# Set the output header
header = ["loan_price", "remaining_months", "repayment_interval", "future_value"]

# Set the output file path
output_path = Path("inexpensive_loans.csv")

# @TODO: Use the csv library and `csv.writer` to write the header row
# and each row of `loan.values()` from the `inexpensive_loans` list.
# YOUR CODE HERE!

