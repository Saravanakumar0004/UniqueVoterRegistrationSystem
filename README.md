Unique Voter Registration System – README


📌 Project Overview

The Unique Voter Registration System is a Java-based console application designed to manage voter registrations efficiently. It allows users to register new voters, view all registered voters, search for a voter, delete voter records, and count the total number of registered voters.

The system uses MySQL as the database and connects through a custom DBConnection class.
(Ref: DBConnection.java DBConnection)

🚀 Features
✅ 1. Register New Voter

Users can enter full voter details such as:

Voter ID

Name

Age

Address

Parent’s Name

Gender

Mobile, Email

Aadhaar

DOB

Nationality

District, State, Pincode

Constituency

Booth No

Voter Type

Auto-generated Registration Date
(Ref: Main.java )


The details are stored in the MySQL voters table using addVoter().
(Ref: VoterRegistrationSystem.java )

✅ 2. View All Registered Voters

Displays voter entries from the database using SQL SELECT * FROM voters.
(Ref: VoterRegistrationSystem.java – showVoters() )

✅ 3. Search Voter by ID

Searches the database using the voter ID and displays their full record.
(Ref: VoterRegistrationSystem.java – searchVoter() )

✅ 4. Delete Voter

Deletes a voter record using their voter ID.
(Ref: VoterRegistrationSystem.java – deleteVoter())

✅ 5. Count Registered Voters

Uses MySQL COUNT(*) to show total registered voters.
(Ref: VoterRegistrationSystem.java – countVoters() )


🗂️ Project File Structure

| File                             | Description                                                                                            |
| -------------------------------- | ------------------------------------------------------------------------------------------------------ |
| **Main.java**                    | Entry point, menu system for all operations.                                                           |
| **DBConnection.java**            | Connects Java to MySQL database.                                                                       |
| **Voter.java**                   | Voter data model with fields, getters, and `toString()`.                                               |
| **VoterRegistrationSystem.java** | Handles all database operations (Add, Read, Search, Delete, Count).                                    |
| **voters.txt**                   | A leftover file from older versions (not used in MySQL version). Contains sample: `v101,Voter@3661bc`  |


🛢️ Database Requirements

Database Name:
voterdb

Table: voters

You must create the table manually:
CREATE TABLE voters (
    voterId VARCHAR(20) PRIMARY KEY,
    name VARCHAR(100),
    age INT,
    address VARCHAR(200),
    fatherMotherName VARCHAR(100),
    gender VARCHAR(20),
    mobile VARCHAR(15),
    email VARCHAR(100),
    aadhaar VARCHAR(20),
    dob VARCHAR(20),
    nationality VARCHAR(50),
    district VARCHAR(50),
    state VARCHAR(50),
    pincode VARCHAR(10),
    constituency VARCHAR(100),
    boothNo VARCHAR(20),
    voterType VARCHAR(20),
    registrationDate VARCHAR(20)
);

⚙️ How to Run

Install MySQL
Create database and table (SQL shown above)
Update MySQL username/password in DBConnection.java if needed
(default USER=root, PASS=root)
Compile program:
javac *.java

Run program:
java Main


📘 Technology Stack

Java (Core Java, OOP)

MySQL Database

JDBC (MySQL Connector/J)

Console-Based UI

📝 Conclusion

This project is a complete, functional voter registration management system using Java and MySQL. It follows object-oriented design principles and performs all essential CRUD operations successfully.

If you want, I can also prepare:

✅ A professional GitHub README design (with badges & screenshots)
✅ A project report (synopsis / abstract / documentation)
✅ UML diagrams (Class Diagram, Use Case, Activity)

Just tell me!

