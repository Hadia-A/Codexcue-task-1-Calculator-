Simple CLI Calculator
This is a simple command-line interface (CLI) calculator implemented in Python. It can perform basic arithmetic operations such as addition, subtraction, multiplication, and division. The calculator also handles decimal inputs and provides appropriate error messages for invalid inputs.

Features:
Addition
Subtraction
Multiplication
Division (with error handling for division by zero)
Continuous operation until the user chooses to exit
Handles both integer and decimal inputs

Prerequisites:
Python 3.x

Usage:
When you run the script, you will be presented with a menu to select the desired operation. You can enter the numbers to perform the calculation, and the result will be displayed. The calculator will continue running until you choose to exit by selecting option 5.

Example Interaction:
mathematica
Copy code
Select operation:
1. Add
2. Subtract
3. Multiply
4. Divide
5. Exit
Enter choice (1/2/3/4/5): 1
Enter first number: 5.2
Enter second number: 3.8
The result is: 9.0
Select operation:
1. Add
2. Subtract
3. Multiply
4. Divide
5. Exit
Enter choice (1/2/3/4/5): 5
Exiting...

Code Explanation:
The main functionality is provided by four functions: add(), subtract(), multiply(), and divide(). These functions perform the respective arithmetic operations.

The main() function contains a loop that continuously prompts the user to select an operation and enter numbers. It handles invalid inputs and ensures the calculator runs smoothly.

python
Copy code
def add(x, y):
    return x + y

def subtract(x, y):
    return x - y

def multiply(x, y):
    return x * y

def divide(x, y):
    if y == 0:
        return "Error: Division by zero"
    return x / y

def main():
    while True:
        print("Select operation:")
        print("1. Add")
        print("2. Subtract")
        print("3. Multiply")
        print("4. Divide")
        print("5. Exit")

        choice = input("Enter choice (1/2/3/4/5): ")

        if choice == '5':
            print("Exiting...")
            break

        if choice in ['1', '2', '3', '4']:
            try:
                num1 = float(input("Enter first number: "))
                num2 = float(input("Enter second number: "))

                if choice == '1':
                    print(f"The result is: {add(num1, num2)}")
                elif choice == '2':
                    print(f"The result is: {subtract(num1, num2)}")
                elif choice == '3':
                    print(f"The result is: {multiply(num1, num2)}")
                elif choice == '4':
                    print(f"The result is: {divide(num1, num2)}")
            except ValueError:
                print("Invalid input. Please enter numeric values.")
        else:
            print("Invalid input. Please select a valid operation.")

if __name__ == "__main__":
    main()
Contributing
If you have any suggestions or improvements, feel free to create a pull request or open an issue.

License
This project is licensed under the MIT License.
