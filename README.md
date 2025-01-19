# Daily-Spending-Tracker
Project Outline: Daily Spending Tracker with Budget Management 
**Project Setup**
  Project Name: Daily Spending Tracker 
  Language: Python 
  Dependencies: pandas (for data manipulation), matplotlib or seaborn (for visualization), datetime (for date handling). 
  **Project Structure** 
  Main Script: spending_tracker.py 
  Data Storage: CSV file (spending_data.csv) to log daily expenses. 
  Configuration File: JSON or YAML file to store budget configurations (budget_config.json). 
**Components Budget Initialization**:  Set up a monthly budget based on the total salary: 45% for needs 25% for discretionary spending 30% for savings 
  Daily Expense Input:  Prompt the user to enter their daily expenses, categorized into needs, discretionary spending, and savings. 
  Save these expenses to the spending_data.csv file. 
**Daily and Monthly Calculation**:  Calculate the total spending for the day. Deduct daily expenses from the respective budget categories. 
    Calculate the remaining budget for each category for the rest of the month. 
**Data Visualization**:  Generate simple plots to visualize: Daily spending trend. Remaining budget for each category. Budget Summary:  Display a summary of the daily total, monthly total, and remaining budget in each category. 
**Data Storage and Retrieval**:  Save daily expenses into a CSV file. Load previous data to update the daily spending and remaining budget.

**code:**
print("Welcome to the Daily Expense Tracker :)")
salary = int(input("What is your monthly salary?\n"))
savings = salary * 30/100
money_to_spend = salary - savings
print(f"You have total ${money_to_spend} for the month")
# Initialize total spent money
total_spent_money = 0

# Example of daily spending; you can replace these with inputs or more dynamic data collection
daily_spent = [200, 450, 350, 2000]  # List of daily expenses

# Add each day's spending to the total
for spent in daily_spent:
    total_spent_money += spent

# Calculate remaining money
left_money = money_to_spend - total_spent_money

print(f"Total spent so far: ${total_spent_money}")
print(f"Remaining money to spend for the month: ${left_money}")
