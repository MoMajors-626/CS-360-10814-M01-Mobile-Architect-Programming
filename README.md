# CS-360-10814-M01 Mobile Architecture and Programming

## Warehouse Hero

Warehouse Hero is an Android inventory app I built to make tracking stock simple. Users can create an account, manage inventory items and quantities, and control optional SMS alerts for inventory updates. The app uses Java, SQLite, RecyclerView, and Material Design components.

## Features

- Create a new user account
- Log in using saved account information
- Add new inventory items
- View saved inventory
- Edit item names and quantities
- Delete inventory items
- Store account and inventory data with SQLite
- Keep inventory data after closing and reopening the app
- Navigate between Inventory and Notifications
- Enable or disable optional SMS alerts
- Handle SMS permission approval or denial
- Log out and return to the login screen

## Technologies Used

- Java
- Android Studio
- SQLite
- RecyclerView
- Material Design
- XML layouts
- SharedPreferences
- Android runtime permissions

## Project Structure

### LoginActivity

Handles account creation and login. User credentials are checked against the SQLite database before the Inventory screen opens.

### GridActivity

Controls the main Inventory screen. Users can add, view, edit, and delete inventory items. This screen also includes navigation to Notifications and Log Out.

### NotificationsActivity

Controls the optional SMS notification settings. Users can enable or disable SMS alerts, and the app responds to whether SMS permission is allowed or denied.

### Database

Manages the SQLite database used by Warehouse Hero. The database stores user accounts and inventory information.

The inventory database supports all four CRUD operations:

- **Create:** Add new inventory items
- **Read:** Display saved inventory items
- **Update:** Change item names or quantities
- **Delete:** Remove inventory items

### InventoryItem

Represents an inventory item and stores its database ID, name, and quantity.

### InventoryAdapter

Connects inventory data to the RecyclerView and controls how each inventory item is displayed.

## Android Configuration

- Minimum SDK: API 34
- Target SDK: API 37
- Compile SDK: API 37
- Version Code: 1
- Version Name: 1.0

## Permissions

Warehouse Hero uses the following optional permission:

```text
android.permission.SEND_SMS
```

The SMS permission is only used for the notification feature. If the user denies SMS permission, the main inventory features continue to work normally.

## Testing

I tested Warehouse Hero using the Android Emulator in Android Studio.

Testing included:

- Creating a new account
- Logging in with valid credentials
- Rejecting incorrect login information
- Closing and reopening the app to verify saved information
- Adding inventory items
- Reading saved inventory
- Updating inventory information
- Deleting inventory items
- Navigating between Inventory and Notifications
- Logging out
- Enabling SMS notifications
- Denying SMS permission
- Making sure inventory still works when SMS permission is denied

## What I Learned

Building Warehouse Hero gave me experience connecting the different parts of an Android application instead of treating each screen as a separate project.

I worked with Java activities, XML layouts, SQLite databases, RecyclerView adapters, CRUD operations, runtime permissions, input validation, navigation, and persistent data.

One of the biggest things I learned was how closely the UI, Java code, and database depend on each other. A small change to a layout ID, database structure, or Java class can affect several other parts of the application, so testing often became an important part of the development process.

## Future Improvements

If I continued developing Warehouse Hero, some features I would consider adding include:

- Barcode scanning
- More advanced low-stock alerts
- Inventory search and filtering
- Multiple warehouse support
- Inventory history
- Cloud backup
- Data exporting
- Inventory reports and statistics
- Additional account security

## Course

**CS 360: Mobile Architecture and Programming**

This project was created to demonstrate the development of a functional Android mobile application using persistent data storage, CRUD database operations, user authentication, navigation, and permission handling.

## Author

**Christopher Majors**
