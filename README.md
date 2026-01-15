# Day-10 - Python-Exception-Handling

Overview

Exception handling in Python allows us to manage runtime errors gracefully without crashing the program.
It ensures smooth execution and helps handle unexpected situations like invalid input, division by zero, or missing files.

Exception handling is widely used in:

 User input validation
 File handling
 APIs and databases
 Production-level applications

Python provides built-in exceptions and tools like `try`, `except`, `else`, and `finally` to handle errors safely.

---

What is an Exception?

An exception is an event that interrupts the normal flow of a program when an error occurs during execution.

If exceptions are not handled, the program terminates abruptly.

---

Common Python Exceptions

 `ZeroDivisionError`
 `ValueError`
 `TypeError`
 `IndexError`
 `KeyError`
 `FileNotFoundError`

---

try…except Block

Python uses `try` and `except` blocks to catch and handle exceptions.

Syntax:

```python
try:
    # code that may raise an exception
except:
    # code that runs if an exception occurs
```

---

Handling ValueError

```python
try:
    num = int(input("Enter an integer: "))
except ValueError:
    print("Number entered is not an integer.")
```

📌 Handles invalid numeric input safely.

---

Handling Multiple Exceptions

```python
try:
    number = int(input("Enter a number: "))
    print(1 / number)
except ZeroDivisionError:
    print("You can't divide by zero!")
except ValueError:
    print("Enter only numbers please!")
except Exception:
    print("Something went wrong!")
```

✔️ Different exceptions can be handled separately for better error messages.

---

The finally Block

The `finally` block always executes, whether an exception occurs or not.

```python
try:
    number = int(input("Enter a number: "))
    print(1 / number)
except ZeroDivisionError:
    print("You can't divide by zero!")
except ValueError:
    print("Enter only numbers please!")
finally:
    print("Do some cleanup here")
```

Used for:

Closing files
Releasing resources
Cleanup tasks

---

Why Exception Handling is Important

 Prevents program crashes
 Improves user experience
 Makes code robust and reliable
 Essential for real-world applications

---

Key Takeaways

 Exceptions interrupt program flow
 Use `try` to test risky code
 Use `except` to handle errors
 Use `finally` for cleanup
 Always handle specific exceptions first

---

Day 10 Completed — Python Exception Handling

