# Smart Campus Resource Booking System — Programming 512

## Running the application
Requires Python 3 with Tkinter and SQLite (standard library). On Windows, open this folder in VS Code and run `python main.py`. Keep all `.py` files and `campus_booking.db` in the same folder. No pip packages are required.

## Features
- Three campuses (Centurion, Pretoria, Umhlanga), each with different maximum durations and opening hours.
- Lecturer registration and password-protected login; staff logins via `staff_setup.py`.
- Role-based permissions through `User`, `Lecturer`, `CampusAdministrator`, and `SystemOperator` classes.
- Administrators manage resources at their assigned campus. Operators can manage and view across campuses. Lecturers can browse resources and create/cancel bookings.
- Bookings are saved in SQLite with dates, start times, durations, campus, resource and lecturer IDs. Overlaps, past dates, out-of-hours bookings, excess durations and maintenance resources are rejected.
- Booking history, campus reports, top resource and average booking duration.

## Demo steps
1. Run `python main.py`, register a lecturer, and log in.
2. Choose **Campus Resources** to view available campus resources.
3. Choose **Bookings / Booking History**, select a campus/resource, enter a future date, start time and duration, then create a booking.
4. Attempt an overlapping booking to see validation. Select a future booking and cancel it.
5. Log in with an administrator to add/update/remove resources and see campus bookings and reports.
6. Log in with an operator to see cross-campus reports.

## Staff accounts
Existing staff accounts in the provided database are preserved. If necessary, run `python staff_setup.py` to create a new administrator or operator. Never publish real passwords or personally identifying student data.

## Project files
- `main.py` — Tkinter interface
- `database.py` — SQLite schema and campuses
- `users.py` — authentication and OOP roles
- `resources.py` — resource management and access checks
- `richfield_campuses.py` — campus data access
- `bookings.py` — booking rules, conflict checks, cancellations and reports
- `staff_setup.py` — staff account setup
- `campus_booking.db` — local persistent database

## Submission
Submit the complete project ZIP via the required Moodle assignment activity. The brief also specifies PDF cover-page/declaration instructions; follow the lecturer's Moodle submission settings. Add your own name, student number, and signature to the official cover page if required. No GitHub requirement is stated in the supplied Programming 512 brief.

