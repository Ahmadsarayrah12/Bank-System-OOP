# 🏦 Bank System OOP Project

A robust, full-featured console-based Banking System built using **C++**. This project demonstrates the practical application of **Object-Oriented Programming (OOP)** principles, clean architecture, and file handling without relying on third-party frameworks.

The system simulates real-world banking operations including client management, transactions, currency exchange, and secure user authentication.

---

## 🚀 Key Features

### 👥 Client Management
* **Full CRUD Operations:** Add, Update, Delete, and Read client information.
* **Search Functionality:** Find clients by Account Number.
* **List Clients:** Display all clients in a formatted table.

### 💸 Transactions
* **Deposit & Withdraw:** Secure balance updates with validation.
* **Transfer:** Transfer funds between clients seamlessly.
* **Transfer Logs:** Automatic recording of all transfer operations.

### 💱 Currency Exchange System
* **Currency Management:** Update rates and manage supported currencies.
* **Exchange Calculator:** Convert amounts between currencies (e.g., USD to JOD) based on current rates.

### 🔐 Security & User Management
* **Authentication:** Secure Login/Logout mechanism.
* **Role-Based Access Control (Permissions):** Admins can assign specific access rights to users (e.g., allow transactions but block client deletion).
* **Data Encryption:** Passwords and sensitive data are encrypted using custom encryption algorithms.
* **Login Register:** Tracks all login attempts (Success/Time/User).

### 🎨 User Interface (UI/UX)
* **Interactive Menu System:** Easy-to-navigate menus separated by logical screens.
* **Colored & Formatted Output:** Utilizes colors to highlight errors, warnings, and success messages for a better user experience.
* **Input Validation:** Robust validation libraries ( `clsInputValidate`) to prevent crashes and ensure data integrity.

---

## 🛠️ Technical Architecture

This project is built following the **"OOP as it Should Be"** roadmap, emphasizing modularity and reusability.

* **Language:** C++ (C++11/C++14 standard).
* **Paradigm:** Object-Oriented Programming.
* **Data Persistence:** Text-file based database (Flat file system).
* **Architecture:**
    * **Presentation Layer (Screens):** Classes prefixed with `cls` (e.g., `clsMainScreen`, `clsDepositScreen`) handle UI and user interaction.
    * **Business Logic Layer (Core):** Classes like `clsBankClient`, `clsUser`, and `clsCurrency` handle the data and rules.
    * **Utility Layer:** Custom-built libraries for validation (`clsInputValidate`), string manipulation (`clsString`), and date handling (`clsDate`).

### 📂 Project Structure Overview
Based on the file organization:
```text
├── Core/
│   ├── clsBankClient.h       # Handles Client logic & file operations
│   ├── clsUser.h             # Handles User logic & permissions
│   ├── clsCurrency.h         # Handles Currency logic
│   └── clsPerson.h           # Base class (Inheritance)
├── Screens/
│   ├── clsMainScreen.h       # Main Menu
│   ├── clsLoginScreen.h      # Auth Screen
│   ├── clsTransactionsScreen.h
│   └── ... (Specific screens for each functionality)
├── Libraries/
│   ├── clsInputValidate.h    # Static methods for input checking
│   ├── clsDate.h             # Date operations
│   ├── clsString.h           # String manipulation
│   └── clsUtil.h             # Encryption & general utilities
└── Data/
    ├── Clients.txt
    ├── Users.txt
    ├── Currencies.txt
    └── ...
