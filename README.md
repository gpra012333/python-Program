# python-Program
# Function to calculate gross salary
def calculate_gross_salary(basic, grade):
    hra = 0.20 * basic
    da = 0.50 * basic
    
    if grade == 'A':
        allowance = 1700
    elif grade == 'B':
        allowance = 1500
    else:
        allowance = 1300
    
    pf = 0.11 * basic
    
    gross_salary = basic + hra + da + allowance - pf
    return gross_salary

# Input data for employees
employee_data = [
    {"basic": 10000, "grade": 'A'},
    {"basic": 4567, "grade": 'B'}
]

# Calculate and display gross salary for each employee
for data in employee_data:
    basic_salary = data["basic"]
    employee_grade = data["grade"]
    gross_salary = calculate_gross_salary(basic_salary, employee_grade)
    print(f"Basic: {basic_salary}, Grade: {employee_grade}, Gross Salary: {gross_salary}")
