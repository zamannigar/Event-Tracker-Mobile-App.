# Event-Tracker-Mobile-App.
Android mobile application for tracking and managing events, featuring user login, data storage, and optional SMS reminders.

# Event Tracker Mobile App

## Project Summary

The goal of my Event Tracker application was to create a functional mobile app that allows users to organize and manage important events. The app was designed to address the need for a simple way to create an account, log in, add events, and keep track of event dates and times. Users can also edit or delete events when their plans change. I included an optional SMS reminder feature so users can receive reminders about upcoming events.

## User-Centered UI Design

Several screens and features were necessary to support the needs of the user. The login screen allows users to create an account or log in with an existing account. After logging in, users can access the Event Manager screen, where they can enter an event name, date, and time. Saved events are displayed in a table with options to edit or delete each event. I also created an SMS notification screen that allows users to enter a phone number, grant SMS permission, send a test reminder, or choose not to use SMS reminders.

I kept users in mind by making the interface straightforward and providing clear labels, buttons, instructions, and feedback messages. For example, the event screen explains the expected date and time formats, and the app displays messages when information is missing or when an action succeeds or fails. SMS notifications are optional, which allows users to continue using the main features of the app without granting additional permissions. These choices helped make the app easier to understand and use.

## Coding Approach

I approached the coding process by separating the application into different activities and responsibilities. I used `MainActivity` for account creation and login, `EventActivity` for managing events, and `SmsPermissionActivity` for SMS reminder functionality. I also created a `DatabaseHelper` class to manage the SQLite database and keep the database operations separate from the user interface code.

Breaking the application into smaller components made the project easier to develop and troubleshoot. I also reused methods for operations such as loading events, adding records, updating records, and deleting records instead of placing all of the logic in one location. In future projects, I can use the same strategy of separating UI, database, and feature logic to make applications easier to maintain and expand.

## Testing and Functionality

I tested the application by running it in Android Studio and checking the major user actions individually. I tested creating accounts, logging in with valid and invalid credentials, adding events, editing events, deleting events, and loading saved information from the SQLite database. I also tested situations where required fields were empty to make sure the app displayed an appropriate message instead of continuing with invalid information.

For the SMS feature, I accounted for whether permission was granted or denied and made sure the rest of the application could still function without SMS permission. Testing is important because an application can compile successfully while still containing problems in its user interactions or logic. Testing different paths helped identify where validation, permission checks, and error handling were necessary.

## Innovation and Challenges

One area where I had to innovate was integrating the optional SMS reminder feature with the event-management portion of the application. The app needed to request Android SMS permission while still allowing users to use the Event Tracker if they denied that permission. I addressed this by separating the SMS functionality from the main event features and providing a "Not Now" option.

I also had to work with event dates and times so a reminder could be scheduled for a future event. This required validating the user's date and time input, checking whether the selected time had already passed, and using Android's `AlarmManager`, `PendingIntent`, and a broadcast receiver to support scheduled reminders.

## Area of Success

I was particularly successful with the database and event-management portion of the application. I created an SQLite database that stores user accounts and event information and implemented the main CRUD operations needed for the app. Users can create events, view saved events, update existing events, and delete events. Connecting these database operations to the user interface demonstrated my understanding of Android development, persistent data storage, event handling, input validation, and user-centered application design.

Overall, this project demonstrates my ability to take a mobile application from an initial UI design through development and testing while combining database functionality, multiple screens, permissions, user feedback, and mobile application features into one working project.
