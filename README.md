# Discount-Calculator

This project demonstrates how to calculate the final price of an item after applying a discount in Python.  
A discount is applied **only if the discount percentage is 20% or higher**. Otherwise, the original price is returned.

---

## Features
- Defines a function `calculate_discount(price, discount_percent)`.
- Applies the discount only if it is **20% or more**.
- Prompts the user to enter:
  - The original price of the item.
  - The discount percentage.
- Prints the final price (after discount) or the original price (if discount < 20%).

---

## Code Example

```python
def calculate_discount(price, discount_percent):
    """
    Calculates the final price after applying discount.
    Discount is applied only if discount_percent >= 20.
    """
    if discount_percent >= 20:
        discount_amount = price * (discount_percent / 100)
        final_price = price - discount_amount
        return final_price
    else:
        return price


# Prompt user for input
try:
    price = float(input("Enter the original price: "))
    discount_percent = float(input("Enter the discount percentage: "))

    final_price = calculate_discount(price, discount_percent)

    if discount_percent >= 20:
        print(f"Final price after {discount_percent}% discount: {final_price:.2f}")
    else:
        print(f"No discount applied. Final price: {final_price:.2f}")

except ValueError:
    print("Please enter valid numeric values for price and discount.")
Example Runs
Case 1: Discount applied
yaml
Copy code
Enter the original price: 100
Enter the discount percentage: 25
Final price after 25.0% discount: 75.00
Case 2: No discount applied
yaml
Copy code
Enter the original price: 80
Enter the discount percentage: 10
No discount applied. Final price: 80.00
Requirements
Python 3.x installed on your machine

Run the Code
Save the file as discount_calculator.py.

Run in terminal/command prompt:

bash
Copy code
python discount_calculator.py
Concepts Learned
Functions: Reusable blocks of code defined with def.

Conditional Statements (if/else): Used to decide whether to apply the discount.

Type Casting (float): Convert user input (string) into numbers for calculations.

Error Handling (try/except): Handle invalid input gracefully.
