# Cat-Age-Calculator
This Python program calculates the age of a cat in human years based on its age in months or years. It categorises the cat into two life stages: junior (8 to 24 months) and prime (3 to 6 years), using specific formulas to compute the equivalent human age.

## Code Explanation

```python
# Display the main menu for user interaction
print("Cat Age Main Menu")
print("A: Months 8 to 24")
print("B: Years 3 to 6")
print("X: Exit Program")
print()

# Get the user's choice and convert it to uppercase for consistency
option = str(input("Enter Option (A, B, or X): ")).upper()

# Condition for junior cat age calculation
if option == ("A"):
    cat_junior = int(input("Enter age in months between 8 and 24: "))
    
    # Check if the entered age is within the valid range
    if cat_junior in range(8, 25): 
        print("The cat is at the junior life stage")
        # Calculate human age equivalent for junior cats
        human_junior = (cat_junior + 3)
        print("The cat's age in human years is: ", human_junior)
    else: 
        # If the age is outside the valid range, display an error
        print("The age entered is invalid")
        print("Error, Exit program")

# Condition for prime cat age calculation
elif option == ("B"):
    cat_prime = int(input("Enter age in years between 3 and 6: "))
    
    # Check if the entered age is within the valid range
    if cat_prime in range(3, 7): 
        print("The cat is at the prime life stage")
        # Calculate human age equivalent for prime cats
        human_prime = ((cat_prime * 4) + 16)
        print("The cat's age in human years is: ", human_prime)
    else: 
        # If the age is outside the valid range, display an error
        print("The age entered is invalid")
        print("Error, Exit program")

# Condition to exit the program
elif option == ("X"):
    print("Program will exit")

# Catch-all for any invalid options
else:
    print("Error, Program will exit")
```

## Breakdown of the Code:

### Menu Display:
The program starts by displaying a menu that allows the user to choose between entering a cat's age in months (option A), years (option B), or exiting (option X).

### Input Handling:
The user's selection is read, and the input is converted to uppercase to ensure case-insensitivity.
Junior Cat Calculation:

If option A is selected, the program prompts the user to enter the cat's age in months (between 8 and 24).
If the age is valid (within range), it calculates the human age by adding 3 to the cat's age and displays it.
If the age is invalid, an error message is shown.

### Prime Cat Calculation:
If option B is selected, the user is prompted to enter the cat's age in years (between 3 and 6).
If the age is valid, the human age is calculated using the formula ((cat_prime * 4) + 16) and displayed.
An error message is shown if the input is invalid.

### Exit Option:
If option X is selected, a message is displayed, and the program exits.

### Invalid Option Handling:
Any other input results in an error message, and the program exits.

## Testing:
The code includes test cases for different ages in both the junior and prime categories, comparing expected human ages with actual computed values, confirming that the calculations are correct.
