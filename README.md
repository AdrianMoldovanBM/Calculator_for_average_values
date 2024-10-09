# Python calculator for average values
Having fun with Python, and using functions in order to create a calculator for computing average values.
Code was written using Google Colab.
The program allows users to input both integers and decimal numbers, and it automatically computes the average.
While tools like Excel can perform this task seamlessly, the focus here is on the underlying code that powers the graphical user interface (GUI). 
It’s the process of building and refining this code that offers valuable insights into programming logic and user interaction.
The code can be improved by adding new functions for different types of calculations, like median values, mode, standard deviation etc.

# Code:
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

# Execution:
    average = calculate_average()

    print(f"The average is: {average}")
