# V-Messenger CLI Chat Application

Welcome to **V-Messenger**, a simple command-line interface (CLI) chat application that allows users to communicate with each other through private and group messaging, manage friends, and handle an inbox for received messages. This README provides an overview of the application, its features, and how to run it.

## Table of Contents

- [Features](#features)
- [Installation](#installation)
- [How to Use](#how-to-use)
- [Code Overview](#code-overview)
- [Contributing](#contributing)
- [License](#license)

---

## Features

- **User Registration and Login**: 
  - Sign up with a unique username and password.
  - Sign in to access chat features.
  
- **Friend Management**:
  - Add or remove friends from your friend list.
  - Display your current list of friends.

- **Private Messaging**:
  - Send messages to individual users.
  - Check your inbox to read all received messages.

- **Group Chat**:
  - Send messages to multiple recipients in a single chat session.

- **User Data**:
  - All user credentials and messages are managed in a simple in-memory data structure (C++ maps and vectors).

## Installation

1. **Prerequisites**: Ensure you have a working C++ compiler installed on your system (e.g., `g++`).
   
2. **Clone the repository**:
   ```bash
   git clone https://github.com/yourusername/v-messenger-cli.git
   cd v-messenger-cli
   ```

3. **Compile the code**:
   Use the following command to compile the source code:
   ```bash
   g++ -o v_messenger main.cpp
   ```

4. **Run the application**:
   ```bash
   ./v_messenger
   ```

## How to Use

Once the application is running, follow these steps:

### 1. Sign Up / Sign In
- **Sign up** for a new account by providing a username and password.
- **Sign in** with your existing credentials.

### 2. Main Menu
After logging in, you will have access to the following features:

- **Inbox**: View all your received messages.
- **Chat**: Send a private message to another user.
- **Friend List**: View, add, or remove friends from your list.
- **Group Chat**: Send messages to multiple friends at once.
- **Log out**: Exit your session and return to the login menu.

### 3. Sending a Message
- **Private Message**: Choose the recipient from your friend list and send a message.
- **Group Message**: Add multiple recipients and send the same message to all.

### 4. Friend Management
- **Add a Friend**: Search for a user by username and add them to your friend list.
- **Unfriend**: Remove a friend from your list.

## Code Overview

The application is structured around a few key classes and functions:

- **Main Application Flow**:
  - `page1()`: Handles user registration, login, and displaying the initial menu.
  - `page2()`: Displays the main chat menu after a successful login.

- **User Management**:
  - The `user` map stores usernames and passwords for sign-up and login verification.
  
- **Friend Management**:
  - The `frnd` class handles adding, displaying, and removing friends. 
  - It also manages sending and receiving messages via the `chat_on` and `inbox` methods.

- **Messaging System**:
  - Each user has an inbox managed by the `inbox` method.
  - Messages are stored and displayed with the sender's name in a simple format.

### Key Classes & Methods

- **`class frnd`**: Handles the friend list and messaging.
  - `addfrnd(string uname)`: Adds a friend.
  - `unfrnd(string uname)`: Removes a friend.
  - `dispfrnd(string uname)`: Displays a user's friend list.
  - `chat_on(string uname, string reciepient, char* message)`: Sends a message to a recipient.
  - `inbox(string uname)`: Displays all messages in the user's inbox.

- **Global Functions**:
  - `page1()`: Initial login and registration page.
  - `page2(string uname)`: Main menu after successful login.

## Contributing

Contributions are welcome! Feel free to submit a pull request or open an issue if you find a bug or have a feature request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

Happy chatting with V-Messenger!
