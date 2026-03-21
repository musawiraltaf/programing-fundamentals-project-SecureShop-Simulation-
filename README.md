# PF Project - Commented SecureShop Source

This package contains a commented version of the uploaded PF project source files for the **SecureShop** console application.

## Included files

### Source files
- `admin.cpp`
- `customer.cpp`
- `employee.cpp`
- `main.cpp`
- `utils.cpp`

### Header files
- `admin.h`
- `employee.h`
- `ui.h`
- `utils.h`
- `customer.h` *(generated from `customer.cpp` because the original `customer.h` was not uploaded)*

## What was added

- File-level documentation comments
- Function-level documentation comments
- A small number of clarifying inline comments in key control-flow areas
- Header guards for the header files
- A generated `customer.h` so the public customer API is documented consistently

## Project overview

SecureShop is a file-based C++ console application with three user roles:

- **Admin**
  - login + OTP simulation
  - user management
  - inventory/bulk operations
  - discount management
  - revenue reporting
  - activity and audit log viewing

- **Customer**
  - registration and login
  - product browsing
  - cart and wishlist management
  - checkout with discount codes
  - order history
  - feedback and support submission

- **Employee**
  - registration and login
  - feedback handling
  - support handling
  - sales viewing
  - low-stock monitoring
  - announcement sending

## Data files expected by the code

The project reads and writes plain-text files such as:

- `admin.txt`
- `customer.txt`
- `employee.txt`
- `catalogue.txt`
- `cart.txt`
- `wishlist.txt`
- `discount.txt`
- `feedback.txt`
- `Support.txt`
- `orderhistory.txt`
- `activity.txt`
- `audit.txt`
- `announcements.txt`
- `otp.txt`
- `extra.txt`

These runtime data files were **not** part of the uploaded source snapshot.

## Important note about missing implementation

The uploaded files included `ui.h`, but no matching UI implementation source file (for example `ui.cpp`) was provided.  
That means the packaged source is now **well documented**, but it may still require the missing UI implementation from your original project in order to compile and link successfully.

## Suggested compile command

If your missing role/data/UI files are present, a typical build command would look like:

```bash
g++ main.cpp admin.cpp customer.cpp employee.cpp utils.cpp ui.cpp -o secureshop
```

Adjust the command to match the files that exist in your local project.

## Output package

This folder is intended to be a cleaned, readable, submission-friendly version of the source you uploaded.
