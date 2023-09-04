# lab_03_assignment

# new line added to vs code..
# Define the employee data as a list of dictionaries
employee_data = [
    {"Employee ID": "161E90", "Name": "Raman", "Age": 41, "Salary (PM)": 56000},
    {"Employee ID": "161F91", "Name": "Himadri", "Age": 38, "Salary (PM)": 67500},
    {"Employee ID": "161F99", "Name": "Jaya", "Age": 51, "Salary (PM)": 82100},
    {"Employee ID": "171E20", "Name": "Tejas", "Age": 30, "Salary (PM)": 55000},
    {"Employee ID": "171G30", "Name": "Ajay", "Age": 45, "Salary (PM)": 44000},
]

def print_employee_data(data):
    print("\nEmployee Table:")
    print("{:<12} {:<10} {:<4} {:<12}".format("Employee ID", "Name", "Age", "Salary (PM)"))
    print("-" * 40)
    for employee in data:
        print("{:<12} {:<10} {:<4} {:<12}".format(employee["Employee ID"], employee["Name"], employee["Age"], employee["Salary (PM)"]))

def sort_employee_data(data, key):
    if key == 1:
        return sorted(data, key=lambda x: x["Age"])
    elif key == 2:
        return sorted(data, key=lambda x: x["Name"])
    elif key == 3:
        return sorted(data, key=lambda x: x["Salary (PM)"])
    else:
        return data

while True:
    print("\nChoose a sorting parameter:")
    print("1. Sort by Age")
    print("2. Sort by Name")
    print("3. Sort by Salary")
    print("4. Exit")
    
    choice = int(input("Enter your choice (1/2/3/4): "))
    
    if choice == 4:
        break
    
    if choice in [1, 2, 3]:
        sorted_data = sort_employee_data(employee_data, choice)
        print_employee_data(sorted_data)
    else:
        print("Invalid choice. Please enter a valid option (1/2/3/4).")
