# internship
calculator python code 
def add(x, y):
    return x + y

def subtract(x, y):
    return x - y

def multiply(x, y):
    return x * y

def divide(x, y):
    if y == 0:
        return "Error: Cannot divide by zero"
    return x / y

def main():
    print("=== Command-Line Calculator ===")
    print("Available operations: +  -  *  /")
    print("Type 'exit' to quit.\n")

    while True:
        operator = input("Enter operator (+, -, *, /) or 'exit' to quit: ").strip()

        if operator.lower() == 'exit':
            print("Exiting calculator")
            break

        if operator not in ['+', '-', '*', '/']:
            print("Invalid operator.\n")
            continue

        try:
            num1 = float(input("Enter first number: "))
            num2 = float(input("Enter second number: "))
        except ValueError:
            print("Invalid number. Please enter numeric values.\n")
            continue

        if operator == '+':
            result = add(num1, num2)
        elif operator == '-':
            result = subtract(num1, num2)
        elif operator == '*':
            result = multiply(num1, num2)
        elif operator == '/':
            result = divide(num1, num2)

        print(f"Result: {result}\n")

if __name__ == "__main__":
    main()
