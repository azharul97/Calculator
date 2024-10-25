print("This Calculator developed by MD.ASHFAQUL ISLAM, Roll: 48, Section:A")
print("Welcome to Multi digit Calculator!")
print("Select operation:")
print("1. Addition")
print("2. Subtraction")
print("3. Multiplication")
print("4. Division")

choice = input("Enter Your Operation Number (1/2/3/4): ")

# Check if the input is a digit and one of the listed operations
if not choice.isdigit() or choice not in ['1', '2', '3', '4']:
    print("Error!!!! Please enter only an operation listed number (1/2/3/4).")
else:
    numbers = input("Enter numbers separated by space: ")
    numbers = [float(num) for num in numbers.split()]

    if choice == '1':
        result = 0
        for num in numbers:
            result += num
        print("Result of Addition:", result)

    elif choice == '2':
        result = numbers[0]
        for num in numbers[1:]:
            result -= num
        print("Result of Subtraction:", result)

    elif choice == '3':
        result = 1
        for num in numbers:
            result *= num
        print("Result of Multiplication:", result)

    elif choice == '4':
        result = numbers[0]
        for num in numbers[1:]:
            if num == 0:
                print("Error! Division by zero.")
                break
            result /= num
        else:
            print("Result of Division:", result)
# Calculator
