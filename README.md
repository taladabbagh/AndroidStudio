# Android Studio Project

This repository contains an Android application I developed at university. It showcases my skills in Android development, problem-solving, and my ability to overcome challenges during the development process. Below, I’ve outlined the project details, a key challenge I faced, and how I addressed it.

## Table of Contents

1. [Project Overview](#project-overview)
2. [Features](#features)
3. [Challenges and Solutions](#challenges-and-solutions)
4. [Installation](#installation)
5. [Usage](#usage)
6. [License](#license)

---

## Project Overview

This Android application is a **Task Manager** that allows users to create, update, and delete tasks. It was built using Android Studio and demonstrates my proficiency in:

- Designing and implementing user interfaces with XML.
- Managing activity lifecycles and navigation.
- Using `Room` database for local data storage.
- Debugging and optimizing Android applications.

---

## Features

- **Task Creation**: Users can add new tasks with a title, description, and due date.
- **Task Management**: Users can update or delete existing tasks.
- **Persistent Storage**: Tasks are stored locally using the `Room` database.
- **Clean UI**: A simple and intuitive user interface built with `ConstraintLayout`.

---

## Challenges and Solutions

### Challenge: Implementing Persistent Storage with Room Database
- **Problem**:  
  During development, I faced issues with implementing persistent storage for tasks. Initially, I used `SharedPreferences`, but it wasn’t suitable for storing structured data like tasks. I needed a more robust solution to store and retrieve tasks efficiently.

- **Solution**:  
  I decided to use the `Room` database, which is part of Android’s Jetpack library. Here’s how I addressed the challenge:
  1. **Defined the Data Model**: I created a `Task` entity class to represent the structure of each task.
  2. **Created the DAO**: I implemented a Data Access Object (DAO) to define methods for accessing the database, such as inserting, updating, and deleting tasks.
  3. **Set Up the Database**: I built the `Room` database class and ensured it was properly initialized in the application.
  4. **Handled Asynchronous Operations**: To avoid blocking the main thread, I used `Coroutines` for database operations, ensuring a smooth user experience.

This approach not only solved the storage issue but also made the app more scalable and maintainable.

---

## Installation

To run this project locally, follow these steps:

1. **Clone the repository**:
   ```bash
   git clone https://github.com/taladabbagh/AndroidStudio.git
   ```

2. **Open the project in Android Studio**:
   - Launch Android Studio.
   - Select `Open an existing Android Studio project`.
   - Navigate to the cloned repository and select the project folder.

3. **Build and run the project**:
   - Connect an Android device or start an emulator.
   - Click the `Run` button in Android Studio to build and deploy the app.

---

## Usage

Once the app is running, you can:
- Add new tasks by clicking the "Add Task" button.
- View, update, or delete existing tasks from the list.
- Observe how tasks are persisted even after closing and reopening the app.

---

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
