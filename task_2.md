# 2. **Create a Basic Menu for Role Selection (Student/Faculty)**

- **Concepts**: Input/Output, Conditional Statements and functions.
- **Why**: Gather input from the user and use function and conditional statements to control which part of the system to execute based on the user’s role.
- **Alternatives**:
    - You could use **dictionaries** or **lists** to represent options and then get the corresponding action. However, the use of simple conditional statements (`if-else`) is more readable and intuitive for beginners.
- **Best Practices**:
    - Validate user input to prevent crashes.
    - Display a **clear menu** and guide users on available options.
    - Use functions to keep the menu logic separate.

- **Output:** In thsi task i created a main menu. The function use the `config.py` file to fetch the constants. The menu shows the greeting message and give user of his related field. The program interacts with the user and takes his input.

```
# Import the constants file to use the constants
import config

# Create a menu for role selection(Faculty or Student)

def role_selection():
    print("Welcome to TrackTally: The Attendance Tracking System")
    print("Please select your role:")
    print("1.Faculty")
    print("2.Student")

    # Get the role input from the user
    choice = input("Enter your Role:")
    if choice == "1":
        return config.FACULTY
    elif choice == "2":
        return config.STUDENT
    else: 
        print("Please enter a valid choice")
        return role_selection()

# Call the role_selection function
role_selection()
```
