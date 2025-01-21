```python
import math

#define calculating values
def calculator():
    print("Welcome to the Basic Calculator")
    print("Select an operation:")
    print("1. Addition (+)")
    print("2. Subtraction (-)")
    print("3. Multiplication (*)")
    print("4. Division (/)")
    print("5. Exponentiation (**) ")
    print("6. Square Root (√)")
    print("7. Exit, Good Bye")

    while True:  # syntax for infinite loop
        # Getting input from the user
        try:
            choice = input("Enter your choice (1/2/3/4/5/6/7): ")

            if choice in ['1', '2', '3', '4', '5', '6', '7']:
                try:
                    if choice == '1':
                        num1 = float(input("Enter the first number: "))
                        num2 = float(input("Enter the second number: "))
                        print(f"The result of {num1} + {num2} is {num1 + num2}")

                    elif choice == '2':
                        num1 = float(input("Enter the first number: "))
                        num2 = float(input("Enter the second number: "))
                        print(f"The result of {num1} - {num2} is {num1 - num2}")

                    elif choice == '3':
                        num1 = float(input("Enter the first number: "))
                        num2 = float(input("Enter the second number: "))
                        print(f"The result of {num1} * {num2} is {num1 * num2}")

                    elif choice == '4':
                        num1 = float(input("Enter the first number: "))
                        num2 = float(input("Enter the second number: "))
                        if num2 != 0:
                            print(f"The result of {num1} / {num2} is {num1 / num2}")
                        else:
                            print("Error: Division by zero is not allowed.")

                    elif choice == '5':
                        num1 = float(input("Enter the base number: "))
                        num2 = float(input("Enter the exponent number: "))
                        print(f"The result of {num1} ** {num2} is {num1 ** num2}")

                    elif choice == '6':
                        num = float(input("Enter the number: "))
                        if num >= 0:
                            print(f"The square root of {num} is {math.sqrt(num)}")
                        else:
                            print("Error: Cannot calculate the square root of a negative number.")

                    elif choice == '7':
                        print("Exiting the calculator. Goodbye!")
                        return

                except ValueError:
                    print("Invalid input. Please enter a valid number.")

            else:
                print("Invalid input. Please select a valid operation.")

            next_calculation = input("Do you want to perform next task? (yes/no): ")
            if next_calculation.lower() != 'yes':
                print("Exiting. Goodbye!")
                break

        except OSError as e:
            print(f"An I/O error occurred: {e}")

# Run the calculator
calculator()

```


```python

```
