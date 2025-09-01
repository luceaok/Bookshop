
# 📚 Bookshop Basket System

A Java-based object-oriented and GUI-integrated system simulating a digital bookshop. It supports customer and admin roles, book browsing, basket management, and file-based data persistence.

---
## 🚀 Features

- 📦 Add books to basket by barcode
- 🧾 View basket contents and total
- 🛒 Purchase simulation
- 👤 Admin and customer roles
- 🔊 Audiobook support
- 📘 Paperback support
- 🖥️ GUI for login and admin operations
- ✅ Input validation

---

## 🧩 Class Overview

### 📖 Core Classes

#### `book.java` (Abstract)
Base class for all book types with shared attributes and a method to update stock quantity.

#### `paperback.java` (Extends `book`)
Represents a paperback book.
- **Attributes**: `condition`, `pageCount`
- **Methods**: `viewPaperbacks()`

#### `audiobook.java` (Extends `book`)
Represents an audiobook.
- **Attributes**: `format`, `listeningLength`
- **Methods**: `viewAudiobooks()`

#### `basket.java`
Handles basket operations:
- Add books by barcode
- Display basket contents
- Calculate total cost
- Clear basket
- Retrieve barcodes for stock updates

---

### 👤 User Classes

#### `user.java` (Abstract)
Base class for `admin` and `customer`.
- **Attributes**: `userId`, `username`, `surname`, `houseNo`, `postcode`, `city`, `userType`

#### `customer.java` (Extends `user`)
Represents a customer.
- **Attributes**: `credit`, `basket`
- **Methods**: `customerInfo()`, `updateCredit()`

#### `admin.java` (Extends `user`)
Represents an admin user.
- **Methods**: `adminInfo()`

---

### 🧑‍💻 GUI Components

#### `loginFrame.java`
- Entry point for the application
- Allows user selection from a dropdown
- Redirects to `adminFrame` or `customerFrame`

#### `adminFrame.java`
- GUI for admin operations
- **Tabs**:
  - **View Books**: Displays all books
  - **New Book**: Form to add new books with validation
- Supports adding:
  - `paperback`, `audiobook`, `ebook`
- Uses enums for dropdowns

---

## ⚠️ Known Issues

- `updateCredit()` uses credit value as identifier
- `newBook()` in `admin.java` is unused
- No validation for stock availability

---

## ✅ Future Enhancements

- Implement `customerFrame` GUI
- Improve file handling
- Add persistent login system
- Use enums more consistently
- Add search and filter functionality

---
