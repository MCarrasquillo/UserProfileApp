# UserProfileApp

## Project Description

* UserProfileApp is an Android application built using Clean Architecture, Jetpack Compose, and Dagger-Hilt. This app allows users to retrieve and display user profile information by entering a user ID. It uses software architecture, dependency management, and modern UI development.

### Architecture Overview

The app follows the principles of Clean Architecture with the following layers:
• Presentation Layer: Handles UI logic using Jetpack Compose and communicates with the Domain layer through ViewModels.
• Domain Layer: Contains business logic and application rules. It is independent of frameworks, ensuring testability and reusability.
• Data Layer: Manages data sources (e.g., mock data or APIs) and abstracts them from the Domain layer using repositories.

### Folder Structure
![Screenshot 2024-12-09 at 6 41 03 PM](https://github.com/user-attachments/assets/c3761cd4-d076-4738-8a53-94352a0d4048)


### Dependency Injection Setup

This app uses Dagger-Hilt for Dependency Injection to manage dependencies efficiently:
1. @HiltAndroidApp: Initializes Hilt at the application level.
2. Modules: Centralizes dependency provisioning using the @Module and @Provides annotations.
• Example: AppModule.kt provides instances of UserDataSource, UserRepository, and GetUserUseCase.

Gradle Setup
• Add Dagger-Hilt plugin in the build.gradle files:

plugins {
    id 'dagger.hilt.android.plugin'
}
dependencies {
    implementation "com.google.dagger:hilt-android:2.44"
    kapt "com.google.dagger:hilt-compiler:2.44"
}

### Usage Instructions

Prerequisites
• Android Studio (Arctic Fox or later)
• Minimum SDK: 21 (Android 5.0)

Steps to Run
1. Clone the repository:

git clone https://github.com/MCarrasquillo/UserProfileApp.git
cd UserProfileApp


2. Open the project in Android Studio.
3. Sync Gradle and build the project.
4. Run the app on an emulator or connected device.

Features Implemented
1. Fetch and Display User Data:
• Enter a user ID to retrieve user details (name and email) from mock data.
2. Error Handling:
• Displays an error message when a user is not found.
3. Modern UI with Jetpack Compose:
• Utilizes declarative UI for an intuitive and efficient design.
4. Dependency Injection:
• Dagger-Hilt integration for clean and scalable dependency management.
5. Loading Indicator:
• Displays a progress indicator during data retrieval.

### Screenshots

![mainscreen](https://github.com/user-attachments/assets/b0183e76-b4ca-4cfb-81c1-21d0b8a958a7)
* Mainscren

![showinfo](https://github.com/user-attachments/assets/97a6d83e-04e6-4213-a539-4555d196892d)
* Show User Info

![loading](https://github.com/user-attachments/assets/dbcf918e-cbba-4938-b29b-d0a6a3315b94)
* loading
  
![please enter valid id toast](https://github.com/user-attachments/assets/64147a8e-8890-4149-9686-293abdd23b04)
* error: please enter valid id toast

![user not found error shown](https://github.com/user-attachments/assets/c8fabf2e-5723-4083-964d-3b7967776659)
* error: user not found

