# simple-calci
def add(x, y):
    return x + y

def subtract(x, y):
    return x - y

def multiply(x, y):
    return x * y

def divide(x, y):
    if y == 0:
        return "Error! Division by zero."
    return x / y

def calculate():
    print("Simple Calculator")
    print("Select operation:")
    print("1. Add")
    print("2. Subtract")
    print("3. Multiply")
    print("4. Divide")

    ch = input("Enter choice [1/2/3/4]: ").strip()

    if ch in ['1', '2', '3', '4']:
        try:
            n1 = float(input("Enter first number: "))
            n2 = float(input("Enter second number: "))
        except ValueError:
            print("Invalid input. Please enter numeric values.")
            return

        if ch == '1':
            print("Result:", add(n1, n2))
        elif ch == '2':
            print("Result:", subtract(n1, n2))
        elif ch == '3':
            print("Result:", multiply(n1, n2))
        elif ch == '4':
            print("Result:", divide(n1, n2))
    else:
        print("Invalid choice. Please select from 1 to 4.")

calculate()
