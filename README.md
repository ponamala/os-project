Secure File Management System (SFMS)

This is a secure, role-based file management system developed in Python. It allows users to register, log in with OTP verification, and perform various file operations based on their roles (admin, user, or guest). The system ensures security through password hashing and file encryption.

Features:

Role-based access with admin, user, and guest permissions.

Secure login system using bcrypt password hashing and OTP verification.

File management options including view, open, rename, move, and delete (based on role).

View file size and last modified time.

Encrypt and decrypt files using the Fernet module from the cryptography package.

Users can change their password after login.

OTP is delivered as a desktop notification using the plyer module.

Role Permissions:

Admins have full access to all operations.
Users can perform most operations except file deletion.
Guests can only view, open, and check file details.

Setup Instructions:

Install the required Python packages: pip install bcrypt cryptography plyer

Run the program: python sfms.py

On first run, the system will automatically:

Create the SQLite database (sfms.db)

Generate an encryption key (secret.key)

File Overview:

sfms.py – Main program file containing all logic

sfms.db – Stores user credentials securely

secret.key – Used for file encryption and decryption

Notes:

OTP is displayed via system notifications, so make sure notifications are enabled.

The program supports Windows, Linux, and macOS platforms.

Encrypted files are saved with a .enc extension, and the original is removed for security.

About the Project:

This project demonstrates practical implementations of authentication, encryption, file operations, and role-based access control in Python.
