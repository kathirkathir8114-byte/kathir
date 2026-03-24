import sys

class TaskManager:
    def __init__(self):
        self.tasks = []

    def add_task(self, task):
        self.tasks.append(task)
        print(f"Added: '{task}'")

    def show_tasks(self):
        if not self.tasks:
            print("\nYour task list is empty!")
        else:
            print("\n--- Your To-Do List ---")
            for index, task in enumerate(self.tasks, 1):
                print(f"{index}. {task}")

def main():
    manager = TaskManager()
    print("Welcome to TaskMaster 1.0")
    
    while True:
        print("\nOptions: [1] Add Task [2] Show Tasks [3] Exit")
        choice = input("Choose an option: ")

        if choice == '1':
            new_task = input("Enter the task: ")
            manager.add_task(new_task)
        elif choice == '2':
            manager.show_tasks()
        elif choice == '3':
            print("Goodbye!")
            sys.exit()
        else:
            print("Invalid choice, try again.")

if __name__ == "__main__":
    main()
