# 🚀 TomatoApp – Food Delivery System (C++)

![Language](https://img.shields.io/badge/Language-C++-blue)
![Architecture](https://img.shields.io/badge/Architecture-Design%20Patterns-green)
![Platform](https://img.shields.io/badge/Platform-Console-lightgrey)

---

## 📌 Overview

A **C++ console-based food delivery system** inspired by platforms like **Zomato** and **Swiggy**.

This project demonstrates **clean architecture and object-oriented design principles** using multiple design patterns:

- Factory Pattern
- Strategy Pattern
- Singleton Pattern
- Facade Pattern

The application simulates a **complete food ordering workflow** including restaurant discovery, cart management, payment processing, and order notification.

---

# ✨ Features

## 👤 User Management

- Create and manage user profiles
- Maintain individual carts for each user

## 🍽 Restaurant Search

- Search restaurants by location
- Browse restaurant menus

## 🛒 Cart System

- Add menu items to cart
- View cart contents
- Calculate order totals

## 📦 Order Types

- Immediate Orders
- Scheduled Orders

## 💳 Payment Strategies

Supports multiple payment methods:

- UPI
- Credit Card

Implemented using the **Strategy Pattern**.

## 🔔 Notification System

Users receive notifications after successful order placement.

## 🚚 Delivery Options

Supports both:

- Delivery Orders
- Pickup Orders

---

# 🏗 System Architecture

The application follows a **layered architecture**.

User
 │
 ▼
TomatoApp (Facade)
 │
 ├── Managers
 │   ├── RestaurantManager
 │   └── OrderManager
 │
 ├── Factories
 │   ├── NowOrderFactory
 │   └── ScheduledOrderFactory
 │
 ├── Strategies
 │   ├── UpiPaymentStrategy
 │   └── CreditCardPaymentStrategy
 │
 └── Services
     └── NotificationService




### Benefits

- Separation of concerns  
- Modular design  
- Easy extensibility  
- Maintainable architecture  

---

# 📂 Project Structure


TOMATO/
│
├── factories/
│   ├── NowOrderFactory.h
│   ├── OrderFactory.h
│   └── ScheduledOrderFactory.h
│
├── managers/
│   ├── OrderManager.h
│   └── RestaurantManager.h
│
├── models/
│   ├── Cart.h
│   ├── DeliveryOrder.h
│   ├── MenuItem.h
│   ├── Order.h
│   ├── PickupOrder.h
│   ├── Restaurant.h
│   └── User.h
│
├── services/
│   └── NotificationService.h
│
├── strategies/
│   ├── CreditCardPaymentStrategy.h
│   ├── PaymentStrategy.h
│   └── UpiPaymentStrategy.h
│
└── utils/
    └── TimeUtils.h


---

# ⚙️ Installation

## Prerequisites

- C++ Compiler (**g++ / Visual Studio**)
- Standard C++ libraries

---

# 🛠 Build Instructions

Clone the repository:
git clone https://github.comyogeshhchavan/Food-tomatoApp.git

cd TomatoApp


Compile the project:


g++ main.cpp -o tomatoapp

---

# ▶ Running the Application
./tomatoapp


The application simulates a **complete food ordering flow**.

---

# 🧪 Example Output
ser: Adityais active. 
Found Restaurant : 
 - Binker
Selected Restauarant : Binker
Item in cart : 
---------------------------------------------
P1 : Chole Bhature : $120
P2 : Samosa : $15
---------------------------------------------
Grand total : $135
Paid $135 using UPI: (1234567890)

Notification : New Deliveryorder places!
________________________________________________________
Order ID: 1
Customer: Aditya
Restaurant: Binker
Items Ordered:
 - Chole Bhature ($120)
 - Samosa ($15)
Total : $135
Scheduled For: Sat Mar 14 00:03:11 2026
Payment Done...!
________________________________________________________


---

# 🧠 Design Patterns Used

| Pattern | Purpose |
|-------|--------|
| Facade Pattern | Simplifies system interaction |
| Factory Pattern | Handles order creation |
| Strategy Pattern | Payment method selection |
| Singleton Pattern | Ensures single manager instance |

These patterns improve:

- Scalability  
- Maintainability  
- Extensibility  

---

# 🚀 Future Enhancements

Possible improvements:

- User authentication system
- Database integration
- GUI-based interface
- Real-time order tracking
- Restaurant rating and review system

---

