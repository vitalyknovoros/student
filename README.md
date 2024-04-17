# student
# Function to add a new student
def add_student(students, name, age, grade):
    students[name] = {'Age': age, 'Grade': grade}

# Function to print all students
def print_students(students):
    print("Student List:")
    for name, info in students.items():
        print(f"Name: {name}, Age: {info['Age']}, Grade: {info['Grade']}")

# Main function
def main():
    students = {}
    while True:
        print("\nOptions:")
        print("1. Add a new student")
        print("2. Print all students")
        print("3. Quit")

        choice = input("Enter your choice: ")

        if choice == '1':
            name = input("Enter student's name: ")
            age = input("Enter student's age: ")
            grade = input("Enter student's grade: ")
            add_student(students, name, age, grade)
            print("Student added successfully!")
        elif choice == '2':
            if not students:
                print("No students added yet.")
            else:
                print_students(students)
        elif choice == '3':
            print("Exiting program.")
            break
        else:
            print("Invalid choice. Please enter a valid option.")

if __name__ == "__main__":
    main()
