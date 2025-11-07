# Todo App 📝

A modern, feature-rich task management application built with Flutter and BLoC state management. This app helps users organize their daily tasks with an intuitive interface and smooth user experience.


## 🌟 Project Overview

Todo App is a cross-platform mobile application designed to help users manage their daily tasks efficiently. The app categorizes tasks into three sections: New Tasks, Done Tasks, and Archived Tasks, providing a clean and organized workflow for task management.

## 🚀 Features

- ✅ **Create Tasks** - Add new tasks with title, date, and time
- ✅ **Task Categories** - Organize tasks into New, Done, and Archived sections
- ✅ **Mark as Done** - Quick action to mark tasks as completed
- ✅ **Archive Tasks** - Archive tasks for future reference
- ✅ **Delete Tasks** - Swipe to dismiss and delete tasks
- ✅ **Persistent Storage** - Local database storage using SQLite
- ✅ **Dark Theme** - Modern dark-themed UI
- ✅ **Bottom Sheet Input** - Elegant task creation interface
- ✅ **Date & Time Picker** - Built-in date and time selection

## 🛠️ Tech Stack

- **Framework:** Flutter 3.35.5
- **Language:** Dart 3.7.0
- **State Management:** BLoC (Business Logic Component) 9.0.0
- **Local Database:** SQLite (sqflite 2.4.2)
- **Additional Packages:**
    - `flutter_bloc: ^9.1.0` - State management solution
    - `conditional_builder_null_safety: ^0.0.6` - Conditional widget rendering
    - `intl: ^0.20.2` - Date formatting and internationalization
    - `cupertino_icons: ^1.0.8` - iOS style icons

## 🏗️ Architecture

The project follows a clean architecture pattern with BLoC for state management:

```
lib/
├── layout/
│   └── todo_app/
│       └── todo_layout.dart          # Main layout with bottom navigation
├── modules/
│   ├── archived_tasks/
│   │   └── archived_screen.dart      # Archived tasks screen
│   ├── done_tasks/
│   │   └── done_tasks_screen.dart    # Completed tasks screen
│   └── new_tasks/
│       └── new_tasks_screen.dart     # Active tasks screen
├── shared/
│   ├── components/
│   │   ├── components.dart           # Reusable UI components
│   │   └── constents.dart            # App constants
│   └── cubit/
│       ├── cubit.dart                # Business logic layer
│       ├── states.dart               # BLoC states
│       └── bloc_observer.dart        # BLoC event observer
└── main.dart                         # App entry point
```

### Key Architectural Components:

1. **Presentation Layer** - UI components and screens
2. **Business Logic Layer** - BLoC cubits managing app state
3. **Data Layer** - SQLite database operations
4. **Shared Components** - Reusable widgets and utilities

## 📂 Folder Structure

```
todoapp/
├── android/                  # Android platform files
├── ios/                     # iOS platform files
├── lib/                     # Main application code
│   ├── layout/             # App layout structure
│   ├── modules/            # Feature modules
│   ├── shared/             # Shared resources
│   └── main.dart           # Entry point
├── test/                    # Unit and widget tests
├── web/                     # Web platform files
├── windows/                 # Windows platform files
├── macos/                   # macOS platform files
├── linux/                   # Linux platform files
├── pubspec.yaml            # Package dependencies
└── analysis_options.yaml   # Linter configuration
```

## 🎯 BLoC States

The app uses the following states to manage UI updates:

- `AppInitialState` - Initial app state
- `ChangeBottomNavBarState` - Navigation state changes
- `CreateDatabaseState` - Database initialization
- `InsertToDatabaseState` - Task insertion
- `GetFromDatabaseState` - Task retrieval
- `UpdateDatabaseState` - Task updates
- `DeleteFromDatabase` - Task deletion
- `ChangeBottomSheetState` - Bottom sheet visibility
- `AppLoadingState` - Loading indicator

## 💾 Database Schema

The app uses SQLite with the following table structure:

```sql
CREATE TABLE tasks (
  id INTEGER PRIMARY KEY,
  title TEXT,
  date TEXT,
  time TEXT,
  status TEXT
)
```

**Status values:** `new`, `done`, `archived`

## 🚦 How to Run the Project

### Prerequisites

- Flutter SDK 3.35.5 or higher
- Dart 3.7.0 or higher
- Android Studio / VS Code with Flutter extensions
- An emulator or physical device

### Installation Steps

1. **Clone the repository**
   ```bash
   git clone https://github.com/Mohmdhamad/todoapp.git
   cd todoapp
   ```

2. **Install dependencies**
   ```bash
   flutter pub get
   ```

3. **Run the app**
   ```bash
   flutter run
   ```

4. **Build for specific platform**
   ```bash
   # Android
   flutter build apk
   
   # iOS
   flutter build ios
   
   # Web
   flutter build web
   ```

## 🧪 Testing

Run the test suite using:

```bash
flutter test
```

The project includes widget tests in the `test/` directory.

## 🎨 UI Features

- **Dark Theme** - Modern dark color scheme with deep orange accents
- **Bottom Navigation** - Quick access to task categories
- **Floating Action Button** - Easy task creation
- **Swipe to Dismiss** - Intuitive task deletion
- **Circular Avatar** - Visual time indicators
- **Empty State** - Friendly messages when no tasks exist

## 🔄 State Management Flow

1. User interacts with UI
2. UI triggers Cubit method
3. Cubit performs database operation
4. Cubit emits new state
5. BlocConsumer rebuilds UI with new state


## 🔮 Future Improvements

- [ ] Add task priority levels (High, Medium, Low)
- [ ] Implement task categories/tags
- [ ] Add search and filter functionality
- [ ] Include task reminders/notifications
- [ ] Add task notes and descriptions
- [ ] Implement dark/light theme toggle
- [ ] Add data backup and restore
- [ ] Include task statistics and analytics
- [ ] Support for recurring tasks
- [ ] Multi-language support
- [ ] Cloud synchronization
- [ ] Task sharing functionality
- [ ] Voice input for tasks

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 👨‍💻 Developer

**Mohamed Hamad**

- GitHub: [@Mohmdhamad](https://github.com/Mohmdhamad)


## 🙏 Acknowledgments

- Flutter team for the amazing framework
- BLoC library maintainers
- The Flutter community for continuous support

---

⭐ Star this repo if you find it helpful!

💬 Feel free to reach out for questions or suggestions!