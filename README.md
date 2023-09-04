# lab_03_assignment

# new line added to vs code..

class Employee:

    def __init__(self, emp_id, name, age, salary):

        self.emp_id = emp_id

        self.name = name

        self.age = age

        self.salary = salary

 

class EmployeeTable:

    def __init__(self):

        self.employees = []

 

    def add_employee(self, employee):

        self.employees.append(employee)

 

    def print_table(self):

        for employee in self.employees:

            print(f"Employee ID: {employee.emp_id}, Name: {employee.name}, Age: {employee.age}, Salary: {employee.salary}")

 

    def sort_table(self, sort_parameter):

        if sort_parameter == 1:

            self.employees.sort(key=lambda x: x.age)

        elif sort_parameter == 2:

            self.employees.sort(key=lambda x: x.name)

        elif sort_parameter == 3:

            self.employees.sort(key=lambda x: x.salary)

        else:

            print("Invalid sorting parameter")

 

if __name__ == "__main__":

    table = EmployeeTable()

    table.add_employee(Employee("161E90", "Raman", 41, 56000))

    table.add_employee(Employee("161F91", "Himadri", 38, 67500))

    table.add_employee(Employee("161F99", "Jaya", 51, 82100))

    table.add_employee(Employee("171E20", "Tejas", 30, 55000))

    table.add_employee(Employee("171G30", "Ajay", 45, 44000))

 

    while True:

        print("\nMenu:")

        print("1. Sort by Age")

        print("2. Sort by Name")

        print("3. Sort by Salary")

        print("4. Exit")

       

        choice = int(input("Enter your choice: "))

 

        if choice == 4:

            break

 

        table.sort_table(choice)

        table.print_table()