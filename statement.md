## PROBLEM STATEMENT 

Managing a blood bank's inventory is a critical process that requires accurate tracking of available blood units and a rapid, error-free method for determining blood compatibility when units are requested. Manual tracking or reliance on complex external systems can lead to delays in dispensing life-saving blood units, stock imbalances (overstocking or critical shortages), and potential errors in matching donor and recipient blood types, which can have severe medical consequences. There is a need for a simple, automated system to efficiently manage inventory and ensure correct compatibility checks.

## SCOPE OF THE PROJECT

This project implements a command-line application for managing a small-scale blood bank inventory. The system is scoped to handle the core functionalities of:

1. Inventory Management: Storing and updating the unit count for all eight major blood types (O+, O-, A+, A-, B+, B-, AB+, AB-). Data persistence is handled using a local CSV file (blood_inventory.csv).

2. Stock Receiving: Facilitating the addition of new blood units from donations.

3. Compatibility Check & Dispensing: Automatically determining which blood types from the current stock are compatible with a recipient's required blood type and allowing for the dispensing of units while updating the inventory.

4. The project is out of scope for managing patient or donor records, scheduling, advanced supply chain management, or integrating with real-time hospital systems.

## TARGET USERS

The primary target users are personnel responsible for the day-to-day operation of a blood bank or a blood storage facility:

1. Blood Bank Technicians/Staff: Who perform the duties of receiving donated units and dispensing compatible units upon request.

2. Inventory Managers: Who need a quick overview of current stock levels for strategic management and reordering.

## HIGH-LEVEL FEATURES 

1. Persistent Inventory Tracking: Stores and retrieves the count of blood units for all 8 blood types using a local CSV file.

2. Real-time Stock Display: Provides a clear, sorted, and up-to-date view of the current blood bank inventory upon request.

3. Stock Addition (Donation Receiving): Allows users to input the type and quantity of newly received blood units, automatically updating the inventory.

4. Blood Compatibility Logic: Implements a robust check based on standard ABO/Rh blood compatibility rules to identify all compatible and available donor types for a specified recipient type.

5. Safe Unit Dispensing: Guides the user to select from available compatible stock and deducts the requested unit quantity from the inventory only after validation.

