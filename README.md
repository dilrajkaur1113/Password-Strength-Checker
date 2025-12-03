# Password-Strength-Checker

🔐 Password Strength Checker

A simple Python-based **Password Strength Checker** that evaluates how strong a password is based on length, uppercase/lowercase letters, digits, and special characters.
This project is perfect for beginners in Cybersecurity and Python programming.

## 🚀 Features

✔ Checks password length  
✔ Detects uppercase & lowercase letters  
✔ Detects numbers  
✔ Detects special characters  
✔ Gives strength rating (Weak / Medium / Strong / Very Strong)  
✔ Beginner-friendly Python code  
✔ No external libraries needed  


## 📌 How Password Strength is Calculated

The checker evaluates the password based on:

| Criteria                      | Points |
| Length >= 8                     | 1 |
| Contains uppercase letters      | 1 |
| Contains lowercase letters      | 1 |
| Contains numbers                | 1 |
| Contains special characters     | 1 |

**Total Score → Strength Level**

- 0–1 → ❌ Weak  
- 2–3 → ⚠ Medium  
- 4 → ✔ Strong  
- 5 → 🔥 Very Strong  

## 🧠 Logic Behind the Checker

The script uses simple Python conditions:

- `any(char.isupper() for char in password)`
- `any(char.islower() for char in password)`
- `any(char.isdigit() for char in password)`
- Check special characters using:  
  special_chars = "!@#$%^&*()-_=+[]{};:'\",.<>?/|`~"

✅ Step 1: Create a Python file

Create file:
nano password_checker.py
 

✅ Step 2: Code (password_checker.py)

import re
password = input("Enter Password: ")
score = 0
if len(password) >= 8:
    score += 1
if re.search(r"[A-Z]", password):
    score += 1
if re.search(r"[a-z]", password):
    score += 1
if re.search(r"[0-9]", password):
    score += 1
if re.search(r"[^A-Za-z0-9]", password):
    score += 1
if score <= 2:
    print("Weak Password ❌")
elif score == 3 or score == 4:
    print("Moderate Password ⚠️")
else:
    print("Strong Password ✅")

✅ Step 3: Run
python3 password_checker.py

🌟 Why This Project?
This is a beginner-friendly project for:
Cybersecurity learners
Python beginners
Ethical hacking students
Portfolio building
GitHub skill improvement
