expenses = {}  # Dictionary to store expenses by date

print("=" * 40)
print("       WELCOME TO EXPENSE TRACKER")
print("=" * 40)

while True:
    print("\nOptions:")
    print("1. Add Expense")
    print("2. View Total Expenses")
    print("3. Exit")

    choice = input("\nEnter your choice (1/2/3): ").strip()

    if choice == "1":
        date = input("Enter the date (e.g. 19-04-2026): ").strip()
        item = input("What did you spend on? ").strip()
        
        try:
            amount = float(input(f"Enter amount spent on '{item}': $"))
        except ValueError:
            print("Invalid amount! Please enter a number.")
            continue

        if date not in expenses:
            expenses[date] = {}  # Create a new dict for that date

        if item in expenses[date]:
            expenses[date][item] += amount  # Add to existing item
        else:
            expenses[date][item] = amount   # New item for that date

        print(f"✅ Added: ${amount:.2f} for '{item}' on {date}")

    elif choice == "2":
        if not expenses:
            print("No expenses recorded yet!")
        else:
            print("\n" + "=" * 40)
            print("        YOUR EXPENSE SUMMARY")
            print("=" * 40)

            grand_total = 0

            for date, items in expenses.items():
                print(f"\n📅 Date: {date}")
                day_total = 0

                for item, amount in items.items():
                    print(f"   - {item}: ${amount:.2f}")
                    day_total += amount

                print(f"   💰 Day Total: ${day_total:.2f}")
                grand_total += day_total

            print("\n" + "-" * 40)
            print(f"   🧾 GRAND TOTAL: ${grand_total:.2f}")
            print("-" * 40)

    elif choice == "3":
        print("\n" + "=" * 40)
        print("  👋 BYE BYE! THANKS FOR COMING!")
        print("=" * 40)
        break

    else:
        print("❌ Invalid choice! Please enter 1, 2, or 3.")
