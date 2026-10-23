Grand Stay: Hotel Reservation System

A terminal-based hotel reservation system written in Python. A receptionist can view rooms, check availability, book and cancel rooms, and all data is saved to a JSON file so nothing is lost when the program closes.

Status: in development. See PLANNING.md for the full plan, data structure, and code flow.

Features

Core

Store rooms (room number, type, price per night)
Check room availability for check-in and check-out dates
Book a room with guest name, phone, and dates
Block overlapping bookings for the same room
Automatic total price (nights x price per night)
Cancel a booking
Save and load all data from a file
Menu that keeps running until Exit
Input checks (no empty fields, no invalid dates or room numbers)

Extra

Search bookings by guest name
Booking summary with total price
Report of all current bookings
Edit an existing booking
How to run
Install Python 3.8 or newer.
Clone this repository and open its folder in a terminal.
Start the program:
python main.py

No extra libraries are needed.

Project structure
hotel-reservation/
├── main.py           # entry point: loads data and starts the menu
├── menu.py           # menu loop and user prompts
├── data.py           # default rooms and data structure
├── logic.py          # booking logic: availability, book, cancel, search, edit
├── storage.py        # save and load the JSON file
├── validators.py     # input checks
├── data/
│   └── hotel_data.json
├── README.md
└── PLANNING.md
How the data is stored

Everything is kept in one JSON file (data/hotel_data.json) with three parts: rooms, bookings, and next_booking_id. Dates are shown to the user as DD-MM-YYYY and stored as YYYY-MM-DD.

Author

[Muhammad Ali]
