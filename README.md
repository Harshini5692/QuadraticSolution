# Weather Modeling using Quadratic Solution

This project demonstrates a simple weather modeling approach using a quadratic equation:

T(t) = a * t^2 + b * t + c

yaml


Where:  
- **T(t)** → predicted temperature at time `t` (hour/day)  
- **a, b, c** → coefficients representing environmental conditions  
- **t** → time input (hour/day)  

The project is implemented in four stages, starting from the most basic (hardcoded values) to handling multiple sets of inputs from a file.

---
 ##Folder Structure
weather_model_quadratic/
version1_hardcoded.py
version2_keyboard_input.py
version3_file_input_single.py
version4_file_input_multiple.py
inputs_single.txt
inputs_multiple.txt
README.md

---

## Versions Implemented

### Version 1: Hardcoded Values  
File: `version1_hardcoded.py`  

```python
# Predict temperature using hardcoded coefficients
a = 0.5
b = -3
c = 28
t = 5  # e.g., 5th hour or 5th day

T = a * t**2 + b * t + c
print(f"Predicted temperature at t={t}: {T:.2f}°C")
Run:

bash

python version1_hardcoded.py
Version 2: Keyboard Input
File: version2_keyboard_input.py

python

a = float(input("Enter coefficient a: "))
b = float(input("Enter coefficient b: "))
c = float(input("Enter coefficient c: "))
t = float(input("Enter time t (hour/day): "))

T = a * t**2 + b * t + c
print(f"Predicted temperature at t={t}: {T:.2f}°C")
Run:

bash

python version2_keyboard_input.py
Version 3: File Input (Single Set)
File: version3_file_input_single.py

Example inputs_single.txt:

diff

0.3
-2.5
26
4
python

with open("inputs_single.txt", "r") as f:
    lines = f.readlines()

a = float(lines[0])
b = float(lines[1])
c = float(lines[2])
t = float(lines[3])

T = a * t**2 + b * t + c
print(f"Predicted temperature at t={t}: {T:.2f}°C")
Run:

bash

python version3_file_input_single.py
Version 4: File Input (Multiple Sets)
File: version4_file_input_multiple.py

Example inputs_multiple.txt:


0.5 -2.0 25 3
0.4 -1.5 28 5
0.2 -0.5 30 2
python

with open("inputs_multiple.txt", "r") as f:
    for line in f:
        a, b, c, t = map(float, line.strip().split())
        T = a * t**2 + b * t + c
        print(f"a={a}, b={b}, c={c}, t={t} -> T={T:.2f}°C")
Run:

bash

python version4_file_input_multiple.py
Example Output:

ini

a=0.5, b=-2.0, c=25.0, t=3.0 -> T=24.50°C
a=0.4, b=-1.5, c=28.0, t=5.0 -> T=29.50°C
a=0.2, b=-0.5, c=30.0, t=2.0 -> T=30.30°C
How to Use
Clone or download the repository.

Ensure Python (>=3.7) is installed.

Run each version with:

bash

python filename.py
Modify input files (inputs_single.txt, inputs_multiple.txt) for your own test cases.

GitHub Setup
To upload this project to GitHub:

bash

# Initialize a new Git repository
git init

# Add all project files
git add .

# Commit changes
git commit -m "Initial commit - Weather Modeling Quadratic Solution"

# Create a new GitHub repository (do this on GitHub site)

# Link local repo to GitHub
git remote add origin https://github.com/your-username/weather_model_quadratic.git

# Push code to GitHub
git branch -M main
git push -u origin main
print(f"Predicted temperature at t={t}: {T:.2f}°C")
