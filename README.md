# Hotel_Management_System-JDBC
🏨 Hotel Reservation System

A Java Console Application that manages hotel room reservations using a MySQL database.
The system allows users to reserve, view, update, and delete reservations, as well as fetch room numbers.

📌 Features

➕ Reserve a Room → Add a new guest reservation

📋 View Reservations → Display all current reservations in a table format

🔎 Get Room Number → Find the room number by reservation ID and guest name

✏️ Update Reservation → Modify guest name, room number, or contact number

❌ Delete Reservation → Remove an existing reservation

🚪 Exit System with a progress effect

🛠️ Technologies Used

Java (JDBC API for database connectivity)

MySQL (Database)

📂 Database Setup

Create a database in MySQL:

CREATE DATABASE hotel_db;
USE hotel_db;


Create a reservation table:

CREATE TABLE reservation (
    reservation_id INT AUTO_INCREMENT PRIMARY KEY,
    guest_name VARCHAR(100) NOT NULL,
    room_number INT NOT NULL,
    contact_no VARCHAR(15),
    reservation_date TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

⚙️ Configuration

Update your database connection credentials in the code:

private static final String url = "jdbc:mysql://127.0.0.1:3306/hotel_db";
private static final String username = "root";
private static final String password = "your_mysql_password";

▶️ How to Run

Compile the project:

javac HotelReservationSystem.java


Run the program:

java HotelReservationSystem


Choose from the menu:

HOTEL MANAGEMENT SYSTEM
1. Reserve a room
2. View Reservations
3. Get Room Number
4. Update Reservations
5. Delete Reservations
0. Exit

📸 Example Output
HOTEL MANAGEMENT SYSTEM
1. Reserve a room
2. View Reservations
3. Get Room Number
4. Update Reservations
5. Delete Reservations
0. Exit
Choose an option: 2

Current Reservations:
+----------------+-----------------+---------------+----------------------+-------------------------+
| Reservation ID | Guest           | Room Number   | Contact Number       | Reservation Date        |
+----------------+-----------------+---------------+----------------------+-------------------------+
| 1              | John Doe        | 101           | 9876543210           | 2025-08-17 10:32:45     |
+----------------+-----------------+---------------+----------------------+-------------------------+

🚀 Future Enhancements

Use PreparedStatement (instead of Statement) to prevent SQL injection.

Add room availability check before booking.

Implement search reservations by guest name.

