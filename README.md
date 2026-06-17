# Budget App Project

A simple Python budget management application that allows users to track deposits, withdrawals, transfers between budget categories, and visualize spending through a text-based chart.

## Features

- Create budget categories (e.g., Food, Clothing, Entertainment)
- Deposit funds into categories
- Withdraw funds from categories
- Transfer funds between categories
- Check available balances
- Generate a percentage-based spending chart
- Display category ledgers in a clean, formatted layout

## Project Structure

```
Budget-app-project/
│
├── budget_app.py
└── README.md
```

## How It Works

### Category Class

Each category maintains:

- A ledger of transactions
- A current balance
- Deposit and withdrawal operations
- Transfers between categories

Example:

```python
food = Category("Food")

food.deposit(1000, "Initial deposit")
food.withdraw(25.50, "Groceries")
```

### Transfers

```python
food.transfer(50, clothing)
```

This will:

- Withdraw money from the source category
- Deposit it into the destination category
- Record both transactions in the ledgers

### Spending Chart

The application can generate a text-based spending chart showing the percentage of spending by category.

Example:

```python
print(create_spend_chart([food, clothing]))
```

Output:

```text
Percentage spent by category
100|
 90|
 80|
 ...
```

## Installation

Clone the repository:

```bash
git clone https://github.com/lucamuratori/Budget-app-project.git
cd Budget-app-project
```

## Usage

Run the application with:

```bash
python budget_app.py
```

The script includes example categories and transactions that demonstrate the application's functionality.

## Example

```python
food = Category("Food")
food.deposit(1000, "deposit")
food.withdraw(10.15, "groceries")

clothing = Category("Clothing")
food.transfer(50, clothing)

print(food)
print(create_spend_chart([food, clothing]))
```

## Technologies Used

- Python 3

## Learning Objectives

This project demonstrates:

- Object-Oriented Programming (OOP)
- Class design
- Data structures (lists and dictionaries)
- String formatting
- Data visualization using plain text

## Future Improvements

- Command-line interface (CLI)
- Persistent storage using files or databases
- Monthly budgeting reports
- Category editing and deletion
- Graphical user interface (GUI)

## License

This project is available for educational and personal use.
