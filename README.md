BLOOD-BANK-CRUD-AND-INVENTORY-SYSTEM
Overview

The Blood Bank Inventory & Compatibility Manager is a Python-based command-line application designed to manage blood stock levels efficiently. Beyond simple inventory tracking, the system includes a medical logic engine that automatically determines blood type compatibility. It ensures that when a recipient needs blood, the system suggests only medically safe donor types (e.g., O- for generic usage, specific matches for others) and manages stock deductions accordingly. The system uses persistent storage (CSV) to ensure inventory data is saved between sessions.
Features

    Inventory Management: View real-time stock levels for all 8 standard blood types (A+, A-, B+, B-, AB+, AB-, O+, O-).

    Smart Compatibility Logic:

    Automatically identifies valid donors for a specific recipient.

Example: If a recipient needs A+, the system checks inventory for A+, A-, O+, and O-.

    Donation Tracking: Add new blood units to the inventory with input validation.

    Safe Dispensing: Prevents dispensing more units than are currently available.

    Data Persistence: automatically generates and updates a blood_inventory.csv file. If the program is closed, data is saved and reloaded upon the next launch.

    Input Validation: Ensures only valid blood types and positive integers are entered to prevent data corruption.

Technologies & Tools Used

    Language: Python 3.x
    Libraries: csv (Built-in): For reading and writing inventory data to the file system. os (Built-in): For file existence checks.
    Interface: Command Line Interface (CLI).

Steps to Install & Run

    Prerequisites You must have Python 3.x installed on your machine.
    Installation A. Download the file blooddndprgm.py. B. Place the file in a folder where you have write permissions (the script needs to create a CSV file in the same directory).
    Running the Application A. Open your terminal (Command Prompt, PowerShell, or Terminal). B. Navigate to the directory containing the script. C. Run the following command: Bash python blooddndprgm.py D. On the first run, the system will automatically create a file named blood_inventory.csv with default stock values.

Instructions for Testing

To ensure the system is working correctly, follow these testing steps:

Test 1: Verify Initial Load

A. Run the program. B. Select Option 1 (Display Current Inventory). C. Verify that you see a list of blood types with default values (e.g., O- should have 15 units).

Test 2: Receive a Donation

A. Select Option 2 (Receive New Units). B. Enter Blood Type: O- (Universal Donor). C. Enter Units: 5. D. The system should confirm the addition. Check Option 1 again to ensure O- is now 20 units (15 + 5).

Test 3: Test Compatibility & Dispensing

A. Select Option 3 (Dispense Units). B. Enter Recipient Blood Type: B+. C. The system should list compatible donors: B+, B-, O+, O-. D. Select a donor type from the list (e.g., O+). E. Enter an amount to dispense (e.g., 2). F. The system should confirm the dispense action.

Test 4: Verify Persistence

A. Select Option 4 to exit the program. B. Run the program again (python blooddndprgm.py). C. Select Option 1. D. Verify that the changes made in Test 2 and Test 3 are still present (The inventory should not have reset to default).
AUTHOR

ABHIJEET PATHAK REG.NO-26MEI10044  INT M.TECH IN COMPUTER SCIENCE AND ENGINEERING VIT BHOPAL
output screenshots
Screenshot 2025-11-23 at 3 28 00 PM Screenshot 2025-11-23 at 3 29 36 PM Screenshot 2025-11-23 at 3 31 37 PM
