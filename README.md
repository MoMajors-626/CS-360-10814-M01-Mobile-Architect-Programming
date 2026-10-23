CS-360-10814-M01 Mobile Architecture and Programming
Warehouse Hero
Warehouse Hero is an Android inventory management app I built to make tracking stock simple. The goal of the project was to create a functional mobile application that allows users to manage inventory without making the interface unnecessarily complicated.

Users can create an account, log in, add inventory items, update item quantities, delete items, and view saved inventory information. The app also includes an optional SMS notification feature that users can enable or disable from the Notifications screen.

Features
Create a new user account
Log in using saved account information
Store user and inventory information with SQLite
Add new inventory items
View saved inventory items
Update item names and quantities
Delete inventory items
Keep inventory data after closing the app
Navigate between Inventory and Notifications
Enable or disable optional SMS alerts
Handle SMS permission approval or denial
Log out and return to the login screen
Technologies Used
Warehouse Hero was developed using:

Java
Android Studio
SQLite
RecyclerView
Material Design components
XML layouts
Android runtime permissions
SharedPreferences
App Structure
The project is separated into several main classes:

LoginActivity
Handles account creation and login. User credentials are checked against the SQLite database before the Inventory screen can be opened.

GridActivity
Controls the main Inventory screen. This activity allows users to add, view, edit, and delete inventory items. It also contains the navigation menu used to open the Notifications screen or log out.

NotificationsActivity
Controls the optional SMS notification settings. Users can enable or disable SMS alerts, and the app handles the Android SMS permission based on the user's choice.

Database
Manages the SQLite database used by Warehouse Hero. The database contains separate tables for user accounts and inventory information.

The inventory database supports the four main CRUD operations:

Create: Add inventory items
Read: Display saved inventory items
Update: Change item names or quantities
Delete: Remove inventory items
InventoryItem
Represents an individual inventory record and stores the item's database ID, name, and quantity.

InventoryAdapter
Connects inventory information to the RecyclerView and controls how individual inventory items are displayed and selected.

Android Support
The current project configuration uses:

Minimum SDK: API 34
Target SDK: API 37
Compile SDK: API 37
Version Code: 1
Version Name: 1.0
Permissions
Warehouse Hero requests the following permission:

android.permission.SEND_SMS
