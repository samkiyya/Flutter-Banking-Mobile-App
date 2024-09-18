# Flutter Banking Mobile App (UI Demo)

![Build Status](https://img.shields.io/github/workflow/status/samkiyya/banking-mobile-app/CI)
![License](https://img.shields.io/github/license/samkiyya/banking-mobile-app)

## Table of Contents

- [Flutter Banking Mobile App (UI Demo)](#flutter-banking-mobile-app-ui-demo)
  - [Table of Contents](#table-of-contents)
  - [Overview](#overview)
  - [Features](#features)
  - [Screenshots](#screenshots)
  - [Technologies Used](#technologies-used)
  - [Setup \& Installation](#setup--installation)
  - [Folder Structure](#folder-structure)
  - [Resources](#resources)
  - [Contributing](#contributing)
  - [Contact](#contact)

## Overview

This is a **UI-only demo** of a banking mobile application developed during my internship project. The app is designed to simulate real-world banking functionalities, providing users with an intuitive and engaging interface for key banking operations. Even though the app doesn't integrate with an actual backend or database, it emulates a realistic user experience by utilizing mock data and map collections to handle actions such as login, transactions, fund transfers, and logout.

**Note:** All interactions, such as user registration, login, account details, and transactions, are simulated using static data stored in map collections. These allow the app to function seamlessly for demonstration purposes without needing a backend.

## Features

- **Welcome Page:** The entry point of the app that introduces users with a smooth transition, leading them to registration or login.
- **Registration & Login:** Users can register and log in using a simulated authentication system where their credentials (username and password) are stored in a map collection. Login functionality is implemented to resemble real-world scenarios.
- **Home Page:** Displays the user’s account summary, including balance and recent transactions, all populated using static data for demonstration.
- **Account Detail:** Provides detailed information about the user’s account, including available balance and recent transaction history, fetched from mock data.
- **Bill Payment:** Simulates paying bills by selecting predefined options. This feature mimics real bill payment processes.
- **Transfer Fund:** Users can simulate transferring funds between accounts. The transactions are reflected within the app using static map collections to emulate real-time fund transfers.
- **Transaction History:** Displays a list of the user’s past transactions. The data is pulled from a mock dataset, providing users with a realistic view of their transaction history.
- **Settings:** Allows users to adjust app preferences and settings. Although preferences are not persisted, the interface mirrors how settings would work in a production app.
- **Support:** Simulates a customer support page where users can access help or assistance, showcasing how a support feature would integrate into a banking app.
- **Drawer Navigation:** Contains buttons that allow users to easily navigate between different sections of the app, including a logout option for secure exit.
- **Logout:** Simulates a real logout process where the user is securely logged out and redirected to the **Welcome Page**. After logging out, there is no option to return to the previous session unless the user logs in again, ensuring a realistic and secure user experience similar to real banking applications.

## Screenshots

Here are sample screenshots of the app, showcasing its features and simulating real banking functionalities despite not having a database:

| Screen                                                      | Description                                                                                                                                                                                 |
| ----------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| ![Welcome](screenshots/welcome.png)                         | **Welcome Page:** The first screen users see when launching the app. It introduces the app and leads users to the login or registration pages.                                              |
| ![Login](screenshots/login.png)                             | **Login Screen:** Users can log in using their registered username and password stored in the app’s map dictionary collection. Authentication is simulated for a realistic experience.      |
| ![Home](screenshots/home.png)                               | **Home Page:** Displays the user’s account balance, recent transactions, and navigation options to other features. Data is populated using mock values for a smooth banking experience.     |
| ![Account Detail](screenshots/account_detail.png)           | **Account Detail:** Shows detailed information about the user’s account, such as available balance and recent transactions. All data is fetched from the simulated map collection.          |
| ![Bill Payment](screenshots/bill_payment.png)               | **Bill Payment:** Users can simulate paying bills by selecting from predefined options. This process mimics a real banking app’s bill payment functionality.                                |
| ![Transaction History](screenshots/transaction_history.png) | **Transaction History:** Shows a list of the user’s past transactions, pulled from mock data. It provides a realistic view of how transactions would appear in a live banking app.          |
| ![Transfer Fund](screenshots/transfer_fund.png)             | **Transfer Fund:** Users can simulate transferring funds between accounts or to another user. The transfer process updates the map collection, giving the illusion of a live fund transfer. |
| ![Settings](screenshots/settings.png)                       | **Settings:** Allows users to update their preferences within the app. Although changes are not persisted, this screen mirrors how a settings page in a live app would function.            |
| ![Support](screenshots/support.png)                         | **Support:** Provides users with a static support page to simulate contacting customer service for assistance with their banking needs.                                                     |
| ![Drawer](screenshots/drawer.png)                           | **Drawer Navigation:** Contains a list of navigation buttons for users to easily switch between different app screens, including a logout button for secure exit.                           |

## Technologies Used

- **Flutter**: Cross-platform framework for developing high-quality apps for iOS and Android from a single codebase.
- **Dart**: The primary programming language used for developing the app.
- **Map Collection:** Used in place of backend database systems for handling user data, transactions, and other functionalities within this demo.

## Setup & Installation

1. **Clone the repository:**

   ```bash
   git clone https://github.com/samkiyya/banking-mobile-app.git
   cd banking-mobile-app
   ```

2. **Install dependencies:**

   ```bash
   flutter pub get
   ```

3. **Run the app:**

   - For Android:

   ```bash
   flutter run
   ```

   - For iOS: Ensure you have an iOS device or simulator set up, then run:

     ```bash
     flutter run --release
     ```

_Note: The `--release` flag is generally used for build and deployment, not for running on an iOS device._

**Note:** All functionalities, including registration, login, account management, transactions, and logout, are simulated using hardcoded values and mock data stored in map collections. There are no real backend services or databases connected in this demo, but the app is designed to mimic the behavior of a real banking application.

## Folder Structure

The project is organized into a clear and logical folder structure to ensure ease of navigation and maintainability. Below is a detailed breakdown:

```bash
lib/
├── animations/                      # Contains custom animations for smooth transitions between screens
│   └── fade_animation.dart          # Defines the fade animation for login and welcome screen transitions
├── controllers/                     # Manages the business logic and state for each screen
│   ├── account_details_controller.dart  # Handles logic related to account details
│   ├── bill_payment_controller.dart     # Manages bill payment functionalities
│   ├── controller_data_layer.dart       # Abstracts data handling and interaction for controllers
│   ├── home_controller.dart             # Manages the logic for the home screen
│   ├── login_controller.dart            # Handles user login processes
│   ├── settings_controller.dart         # Manages user settings and preferences
│   ├── support_controller.dart          # Handles customer support functionalities
│   ├── trans_history_controller.dart    # Manages transaction history logic
│   ├── transfer_funds_controller.dart   # Handles fund transfer operations
│   └── welcome_controller.dart          # Manages logic for the welcome and onboarding screens
├── models/                          # Defines data structures and models for the application
│   ├── account_details_model.dart      # Model representing user account details
│   ├── bill_payment_model.dart         # Model for bill payment information
│   ├── home_model.dart                 # Model for home screen data
│   ├── login_model.dart                # Model for user login data
│   ├── models_data_layer.dart          # Abstracts data handling for models
│   ├── settings_model.dart             # Model for application settings
│   ├── support_model.dart              # Model for customer support data
│   ├── trans_history_model.dart        # Model for transaction history data
│   ├── transfer_funds_model.dart       # Model for fund transfer data
│   └── welcome_model.dart              # Model for welcome and onboarding data
├── utilities/                       # Utility widgets and helper functions used across the app
│   └── background_widget.dart       # Provides a consistent background for screens
├── view/                            # Contains all UI components and screens
│   ├── account_details_screen.dart    # UI for displaying account details
│   ├── bill_payment_screen.dart       # UI for bill payment functionality
│   ├── home_screen.dart               # UI for the home page
│   ├── login_screen.dart              # UI for user login
│   ├── screen_package.dart            # Contains reusable screen components
│   ├── settings_screen.dart           # UI for user settings
│   ├── support_screen.dart            # UI for customer support
│   ├── transaction_history_screen.dart # UI for viewing transaction history
│   ├── transfer_funds_screen.dart      # UI for fund transfer
│   └── welcome_splash_screen.dart      # UI for the initial welcome screen
├── main.dart                        # The main entry point of the application
assets/
├── images/                          # Directory for application assets like images
│   └── logo.png                     # Application logo
screenshots/                         # Directory containing screenshots for the README
```

### Highlights

- **`controllers/`**: Manages the business logic and state for each screen, keeping the UI and business logic separate.
- **`models/`**: Defines data structures and abstracts data handling, ensuring a clean separation between data and presentation layers.
- **`utilities/`**: Contains reusable components and helper functions to avoid code duplication and maintain consistency.
- **`view/`**: Houses all UI components and screens, providing a clear structure for managing different views of the application.

This organization facilitates easy navigation and modification, ensuring that the codebase remains clean and maintainable.

## Resources

If this is your first Flutter project, here are some resources to help you get started:

- [Write Your First Flutter App](https://docs.flutter.dev/get-started/codelab): A step-by-step guide to building your first Flutter app.
- [Flutter Cookbook](https://docs.flutter.dev/cookbook): A collection of useful Flutter samples and recipes.

For additional help with Flutter development, view the [Flutter online documentation](https://docs.flutter.dev/), which includes tutorials, samples, and a comprehensive API reference.

## Contributing

If you'd like to contribute to the project, feel free to submit a pull request or raise an issue to suggest improvements or additional features to enhance the UI demonstration.
Contributions are welcome! Please follow these steps:

1. Fork the repository.
2. Create a new branch for your changes.
3. Submit a pull request with a detailed description of your changes.

For issues or suggestions, open an issue on GitHub.

## Contact

If you have any questions or feedback, feel free to reach out!

- **LinkedIn**: [Samuel Aberra](https://linkedin.com/in/samkiyya)
- **GitHub**: [Samkiyya](https://github.com/samkiyya)
- **Email**: <samuelabera523@gmail.com>
