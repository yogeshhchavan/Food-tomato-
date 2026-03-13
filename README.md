# TomatoApp - Food Delivery System

A simple C++ console-based application simulating a food delivery platform similar to Zomato or Swiggy. This project demonstrates object-oriented design principles, including factories, managers, strategies, and the facade pattern.

## Features

- **User Management**: Create and manage user profiles with carts.
- **Restaurant Search**: Search restaurants by location.
- **Menu Management**: Add and view menu items for each restaurant.
- **Cart Functionality**: Add items to cart, view cart contents, and calculate totals.
- **Order Types**: Support for immediate ("now") and scheduled orders.
- **Payment Strategies**: Multiple payment methods (UPI, Credit Card).
- **Order Processing**: Process payments and send notifications.
- **Delivery and Pickup**: Support for different order types (Delivery, Pickup).

## Project Structure

```
TOMATO/
├── factories/          # Factory classes for creating orders
│   ├── NowOrderFactory.h
│   ├── OrderFactory.h
│   └── ScheduledOrderFactory.h
├── managers/           # Singleton managers for orders and restaurants
│   ├── OrderManager.h
│   └── RestuarantManager.h
├── models/             # Data models
│   ├── Cart.h
│   ├── DeliveryOrder.h
│   ├── MenuItem.h
│   ├── Order.h
│   ├── PickupOrder.h
│   ├── Restaurant.h
│   └── User.h
├── services/           # Notification service
│   └── NotificationService.h
├── strategies/         # Payment strategy pattern
│   ├── CreditCartPaymentStrategy.h
│   ├── PaymentStrategy.h
│   └── UpiPaymentStrategy.h
└── utils/              # Utility classes
    └── TimeUtils.h
```

## Installation and Setup

### Prerequisites
- C++ compiler (e.g., g++ on Linux/Mac, Visual Studio on Windows)
- Standard C++ libraries (included with compiler)

### Compilation
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/tomatoapp.git
   cd tomatoapp
   ```

2. Compile the project:
   ```bash
   g++ main.cpp -I. -ITOMATO -o tomatoapp
   ```
   *Note: This assumes all header files are in the same directory or properly included. You may need to adjust include paths or use a build system like CMake for larger projects.*

### Running the Application
```bash
./tomatoapp
```

The application will simulate a user ordering food from a restaurant in Delhi.

## Usage

The application demonstrates a complete flow:
1. Initialize sample restaurants
2. Create a user
3. Search for restaurants by location
4. Select a restaurant
5. Add items to cart
6. Checkout and process payment
7. Send notification

Example output:
```
User: Aditya is active.
Found Restaurant :
 - Binker
Selected Restauarant : Binker
Item in cart :
---------------------------------------------
P1 : Chole Bhature : $120
P2 : Samosa : $15
---------------------------------------------
Grand total : $135
```

## Design Patterns Used

- **Facade Pattern**: `TomatoApp` class provides a simplified interface
- **Factory Pattern**: Order creation factories
- **Strategy Pattern**: Payment strategies
- **Singleton Pattern**: Managers for orders and restaurants

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Future Enhancements

- Add more payment methods
- Implement user authentication
- Add database persistence
- Create a GUI interface
- Add real-time order tracking
- Implement rating and review system

---

*This is a demonstration project for learning C++ and design patterns. Not intended for production use.*
