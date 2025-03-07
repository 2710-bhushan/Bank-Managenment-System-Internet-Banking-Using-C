**Bank Management System (Internet Banking) Using C with Drawing Prompt**

### **Introduction**
The banking sector has evolved significantly with the advancement of technology, shifting from traditional banking to digital banking. Internet banking enables users to perform financial transactions, check account balances, and manage their finances remotely. This project aims to develop a **Bank Management System (Internet Banking) using C programming** with graphical elements using drawing functions.

### **Objective**
The primary objective of this project is to build a robust banking management system that allows users to interact with an interface for performing banking transactions. The inclusion of graphical elements using C’s drawing functions enhances user experience and visual appeal.

### **Features of the System**
1. **User Authentication:**
   - Login and registration system for customers.
   - Admin authentication for managing accounts.

2. **Account Management:**
   - Account creation (Savings, Current, Fixed Deposit).
   - Account deletion.
   - Update account details.

3. **Transaction Management:**
   - Deposits and withdrawals.
   - Fund transfers.
   - Mini statements and transaction history.

4. **Graphical Representation:**
   - Graphical dashboard to display account balance trends.
   - Pie chart representation of expenses and savings.
   - Visual indicators for account status.

5. **Security Measures:**
   - Encrypted passwords.
   - OTP-based authentication.
   
### **Implementation Details**

#### **Programming Language**
- The system is developed using **C programming**.
- Uses file handling for data storage.
- Utilizes graphics libraries like **graphics.h** in Turbo C/C++ for drawing.

#### **Modules**
1. **User Registration & Login**
   - Input validation to ensure strong password criteria.
   - Secure storage of login credentials.
   
2. **Dashboard and Graphical Representation**
   - **Graphical Balance Display:** Using line graphs to show balance fluctuations.
   - **Pie Charts:** To visualize transaction types (withdrawal, deposit, transfer).
   - **Animated Icons:** Icons for deposit, withdrawal, and transfer transactions.

3. **Transaction Processing**
   - Users can deposit, withdraw, and transfer money.
   - Transaction logs are maintained in files.
   - Confirmation pop-ups using graphical dialogs.

4. **Security & Encryption**
   - MD5 or SHA hashing for storing passwords securely.
   - OTP validation using a random number generator.

### **Graphical Implementation Using C**
The graphical elements of the system are implemented using **graphics.h**. The following drawing functions are used:

1. **`circle(x, y, radius);`** - Used to draw graphical representations like buttons and icons.
2. **`rectangle(x1, y1, x2, y2);`** - Used for drawing login forms and dashboards.
3. **`line(x1, y1, x2, y2);`** - Used for balance trend representation.
4. **`setcolor(COLOR);`** - Used to enhance UI aesthetics.
5. **`outtextxy(x, y, "Text");`** - Displaying text with positioning.

### **File Handling for Data Storage**
- The banking data (account details, transactions) is stored in **binary files**.
- Functions like `fwrite()`, `fread()`, `fseek()`, and `ftell()` are used.
- Data is structured using C **structs**.

### **Sample Code Snippet**
```c
#include <stdio.h>
#include <graphics.h>
#include <conio.h>

void drawDashboard() {
    int gd = DETECT, gm;
    initgraph(&gd, &gm, "C:\\Turboc3\\BGI");
    
    setcolor(WHITE);
    rectangle(50, 50, 400, 300);
    outtextxy(100, 100, "Welcome to Online Banking");
    getch();
    closegraph();
}

int main() {
    drawDashboard();
    return 0;
}
```

### **Challenges and Solutions**
1. **Security Concerns:** Data encryption and user authentication measures were implemented.
2. **Graphical Compatibility:** Used `graphics.h`, but modern alternatives like OpenGL can be explored.
3. **Performance Optimization:** Efficient file handling techniques were adopted to minimize data retrieval latency.

### **Conclusion**
The **Bank Management System** developed using **C programming** provides an interactive and secure platform for managing bank accounts. The inclusion of graphical elements makes it user-friendly and visually appealing. With further advancements, integrating databases and mobile platforms can enhance the system’s usability and scalability.

This project serves as a foundation for understanding **banking system functionalities, C programming concepts, and graphical programming techniques**.

