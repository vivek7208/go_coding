# 🚀 Go Language Conference Booking System

This repository contains a simple Go application 📜 that simulates a conference booking system. 📅 The application allows users to book tickets 🎟️ for a conference named "Go Conference". The booking details are stored in memory 💾 and not persisted in any database.

## 📑 Application Overview

The application is designed around a conference with a total of 50 tickets. It exposes a simple text-based user interface that prompts users to enter their details and book tickets. The user details required are:

- First Name 👤
- Last Name 👥
- Email Address 📧
- Number of Tickets 🎟️

Once the user provides valid input, the application books the tickets and deducts the number of booked tickets from the total available tickets. The application also simulates sending a ticket to the user's email address (note that no actual email is sent).

## 🛠️ Code Overview

### Import Statements

The `main.go` file begins with importing necessary packages:

- `fmt` for formatted I/O operations.
- `sync` to allow multiple goroutines to work with the same variable.
- `time` to simulate the time taken to send the tickets.

### Constants and Variables

The file defines several constants and variables at the top:

- `conferenceTickets` and `conferenceName` to store the total tickets available and the name of the conference.
- `remainingTickets` to keep track of how many tickets are still available.
- `bookings` is a slice that stores all the bookings made by users.
- `UserData` is a struct type that represents a user's data.
- `wg` is a WaitGroup from the `sync` package. It's used to ensure that the program doesn't exit before the simulated email sending goroutine finishes its execution.

### Main Function

The `main()` function is the entry point of the program. It first calls the `greetUsers()` function to display a welcome message to the users. Then it gets the user input, validates it, books the ticket if the input is valid, and sends the ticket.

### Helper Functions

There are several helper functions that are used to perform specific tasks:

- `greetUsers()`: Displays a welcome message to the users.
- `getFirstNames()`: Returns a slice containing the first names of all users who have booked tickets.
- `getUserInput()`: Prompts the user to enter their details and returns them.
- `bookTicket()`: Books the ticket by updating the `remainingTickets` and `bookings` variables.
- `sendTicket()`: Simulates the process of sending the ticket to the user's email. This function is run as a goroutine.

Please note that Go, being a statically-typed, compiled language, is not based on the Object-Oriented Programming (OOP) paradigm like Python or Java. Instead, it utilizes its own unique paradigms and concepts. However, it does support struct types which can have methods associated with them, somewhat similar to classes in OOP.

## 🚀 Getting Started

### Requirements

- Go 1.x 🏁

### Installation

1. Clone this repository to your local machine using the following command:

```bash
git clone https://github.com/vivek7208/go_coding.git
```

2. Navigate into the cloned repository:

```bash
cd go_coding
```

3. Run the application:

```bash
go run main.go
```

## 🎮 Application Usage

Once the application is running, follow the on-screen prompts to book tickets for the "Go Conference". You will need to provide your first name, last name, email address, and the number of tickets you wish to book.

Note: The application checks for basic validation such as whether the name is too short or the email address doesn't contain the "@" sign. It also checks that the number of tickets requested is available.

## 📜 License

This project is open-sourced software licensed under the MIT license.

---
