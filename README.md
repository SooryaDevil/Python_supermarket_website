# Python_supermarket_website
 A menu driven supermarket system using python where user can add items to their list, delete items from their list and display the current items on the list.
# Initialize an empty shopping list
shopping_list = []

def display_menu():
    print("\nSupermarket System Menu:")
    print("1. Add item to the list")
    print("2. Delete item from the list")
    print("3. Display current items in the list")
    print("4. Quit")

def add_item():
    item = input("Enter the item you want to add: ")
    shopping_list.append(item)
    print(f"{item} has been added to your shopping list.")

def delete_item():
    item = input("Enter the item you want to delete: ")
    if item in shopping_list:
        shopping_list.remove(item)
        print(f"{item} has been removed from your shopping list.")
    else:
        print(f"{item} is not in your shopping list.")

def display_list():
    if not shopping_list:
        print("Your shopping list is empty.")
    else:
        print("\nCurrent items in your shopping list:")
        for index, item in enumerate(shopping_list, start=1):
            print(f"{index}. {item}")

while True:
    display_menu()
    choice = input("Enter your choice (1/2/3/4): ")

    if choice == '1':
        add_item()
    elif choice == '2':
        delete_item()
    elif choice == '3':
        display_list()
    elif choice == '4':
        print("Thank you for using the Supermarket System. Goodbye!")
        break
    else:
        print("Invalid choice. Please select a valid option (1/2/3/4).")

