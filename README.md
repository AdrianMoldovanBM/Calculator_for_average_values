
def calculate_average():
    
    try:
        # Prompting the user to enter numbers separated by spaces
        user_input = input("Enter numbers separated by spaces: ")

        # Spliting the input string into individual number strings
        number_strings = user_input.split()

        # Converting the number strings to floats
        numbers = [float(num) for num in number_strings]

        # Calculating the average
        if not numbers:
            return 0  # Return 0 if no numbers are entered

        # The process of calculation
        total = sum(numbers)
        count = len(numbers)
        average = total / count

        return average

    # Dealing with invalid inputs
    except ValueError:
        return "Invalid input. Please enter valid numbers."

# Implementation:
average = calculate_average()

print(f"The average is: {average}")
