# Inventory Management Software

## Overview

This project consists of a command-line inventory management application developed in Python for a vegan products store.

The software allows users to:

- manage product inventory;
- register new products;
- record completed sales;
- calculate gross and net profits;
- persist inventory and sales data across multiple executions using a JSON file.

The project was developed following a predefined specification, with particular attention to clean code, input validation, modular programming, and data persistence.

---

## Technologies

- Python 3
- JSON (data persistence)
- Command-Line Interface (CLI)

---

## Project Requirements

### Inventory Management Software for a Vegan Products Store

The software must provide the following features:

- Register new products, including:
  - product name;
  - quantity;
  - selling price;
  - purchase price.
- List all products currently in stock.
- Record completed sales.
- Display gross and net profits.
- Display a help menu with all available commands.

The application is **text-based**, so it must be operated from the command line.

---

## Example Program Interaction

```text
Enter a command: help

Available commands:
add: add a product to the inventory
list: list all products in the inventory
sale: record a completed sale
profits: show total profits
help: display the available commands
exit: close the program
```

```text
Enter a command: add

Product name: soy milk
Quantity: 20
Purchase price: 0.80
Selling price: 1.40

ADDED: 20 X soy milk
```

```text
Enter a command: add

Product name: tofu
Quantity: 10
Purchase price: 2.20
Selling price: 4.19

ADDED: 10 X tofu
```

```text
Enter a command: add

Product name: seitan
Quantity: 5
Purchase price: 3.00
Selling price: 5.49

ADDED: 5 X seitan
```

```text
Enter a command: list

PRODUCT         QUANTITY    PRICE
soy milk        20          €1.40
tofu            10          €4.19
seitan          5           €5.49
```

```text
Enter a command: sale

Product name: soy milk
Quantity: 5

Add another product? (yes/no): yes

Product name: tofu
Quantity: 2

Add another product? (yes/no): no

SALE RECORDED

- 5 X soy milk: €1.40
- 2 X tofu: €4.19

Total: €15.38
```

```text
Enter a command: list

PRODUCT         QUANTITY    PRICE
soy milk        15          €1.40
tofu            8           €4.19
seitan          5           €5.49
```

```text
Enter a command: sale

Product name: seitan
Quantity: 5

Add another product? (yes/no): no

SALE RECORDED

5 X seitan: €5.49

Total: €27.45
```

```text
Enter a command: list

PRODUCT         QUANTITY    PRICE
soy milk        15          €1.40
tofu            8           €4.19
```

```text
Enter a command: profits

Profit: gross = €42.83    net = €19.43
```

```text
Enter a command: cancel

Invalid command.

Available commands:
add: add a product to the inventory
list: list all products in the inventory
sale: record a completed sale
profits: show total profits
help: display the available commands
exit: close the program
```

```text
Enter a command: exit

Bye bye
```

---

## Technical Requirements

- Organize the application into dedicated functions.
- Persist inventory and sales data across program executions.
- Validate all user inputs and handle invalid values through exceptions.
- Verify product availability before recording a sale.
- Increase the quantity of existing products instead of creating duplicates.
- Compute:
  - **Gross profit** as the total revenue from sales.
  - **Net profit** as gross profit minus the purchase cost of sold products.
- Follow the specification exactly, reproducing the required outputs.
- Use English identifiers following the **snake_case** naming convention.
- Document all functions, classes and methods using **docstrings**.

---

## Project Structure

```text
inventory-management/
│
├── README.md
├── inventory_management.py
└── inventory.json
```

---

## How to Run

Run the application from the command line:

```bash
python inventory_management.py
```

Follow the on-screen instructions to manage the inventory, register sales and display profits.
