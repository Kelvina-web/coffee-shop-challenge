# ☕ Coffee Shop Challenge

A Python-based object-oriented simulation of a coffee shop, modeling relationships between customers, coffees, and orders.

## 📋 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Testing](#testing)
- [Contributing](#contributing)
- [License](#license)
- [Author](#author)

## 📖 Overview

This project models a coffee shop scenario using Python classes to represent `Customer`, `Coffee`, and `Order`. It emphasizes object relationships, data validation, and aggregate functions to simulate real-world interactions within a coffee shop environment.

## ✨ Features

- **Customer Class**:
  - Name property with type and length validation (1–15 characters).
  - Methods to retrieve associated orders and unique coffees.
  - Ability to create new orders.

- **Coffee Class**:
  - Immutable name property with minimum length validation (≥3 characters).
  - Methods to retrieve associated orders and unique customers.
  - Aggregate functions to compute total orders and average price.

- **Order Class**:
  - Associates a customer with a coffee and a price (float between 1.0–10.0).
  - Immutable price property with type and range validation.

- **Bonus**:
  - Class method to determine the customer who spent the most on a specific coffee.

## 🛠 Installation

1. **Clone the Repository**:

   ```bash
   git clone https://github.com/your-username/coffee-shop-challenge.git
   cd coffee-shop-challenge
   ```

2. **Set Up Virtual Environment**:

   ```bash
   pipenv install
   pipenv shell
   ```

   *Ensure you have [Pipenv](https://pipenv.pypa.io/en/latest/) installed.*

## 🚀 Usage

To interact with the classes and test functionality:

```bash
python debug.py
```

Within `debug.py`, you can create instances and invoke methods, for example:

```python
from customer import Customer
from coffee import Coffee
from order import Order

# Create instances
customer1 = Customer("Alice")
coffee1 = Coffee("Espresso")
order1 = Order(customer1, coffee1, 3.5)

# Access data
print(customer1.orders())
print(coffee1.average_price())
```

## 🗂 Project Structure

```
coffee-shop-challenge/
├── Pipfile
├── Pipfile.lock
├── debug.py
├── customer.py
├── coffee.py
├── order.py
└── tests/
    ├── customer_test.py
    ├── coffee_test.py
    └── order_test.py
```

- `customer.py`: Defines the `Customer` class.
- `coffee.py`: Defines the `Coffee` class.
- `order.py`: Defines the `Order` class.
- `debug.py`: Script for manual testing and debugging.
- `tests/`: Contains unit tests for each class.

## ✅ Testing

To run the test suite:

```bash
python -m unittest discover -s tests
```

Ensure all tests pass to validate the correctness of your implementations.

## 🤝 Contributing

Contributions are welcome! Please fork the repository and submit a pull request for any enhancements or bug fixes.

## 📄 License

This project is licensed under the [MIT License](LICENSE).

## 👩‍💻 Author

**Kelvina**

Feel free to reach out for any questions or collaboration opportunities.
