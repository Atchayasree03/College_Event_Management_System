CampusEvents – College Event Management System

A single-file, front-end web app for managing college events: browse, register, and administer events. No build step, no dependencies, no backend.

Features

Students

Browse all events as cards with date, time, venue, department and description
Search by title, venue, department or description
Filter by category and sort by soonest date or most seats left
Live seat counter with a progress bar; events close automatically when full
Register with name, roll number, department and email (validated)
Duplicate registrations for the same event are blocked
"My Registrations" tab to view and cancel sign-ups

Admin (PIN: 1234)

Add, edit and delete events
View registered count against capacity for every event
Deleting an event also removes its registrations

General

Responsive layout for phones and desktops
Automatic light and dark theme
Data persists in the browser via localStorage
Sample events are pre-loaded on first run
Getting started
Save college-events.html to a folder.
Double-click it to open in any modern browser (Chrome, Edge, Firefox, Safari).

To host it, upload the file to GitHub Pages, Netlify, Vercel or any static host.

Project structure
college-events.html   # HTML + CSS + JavaScript, all in one file
README.md
How it works
Part	Details
Storage	localStorage under the key campus_events_v1
Data model	{ events: [...], regs: [...], next: <id counter> }
Event	id, title, cat, dept, date, time, venue, cap, desc
Registration	eid, name, roll, dept, email
Rendering	Plain JavaScript re-renders the lists after every change
Safety	All user text is HTML-escaped before display
Customisation
Change the admin PIN: search for '1234' in the script and replace it.
Reset all data: run localStorage.removeItem('campus_events_v1') in the browser console and refresh.
Edit sample events: change the seed object near the top of the script.
Change colours: edit the CSS variables in :root (--accent, --bg, and so on).
Limitations
Data lives only in the browser it was entered in. It is not shared between users or devices.
The admin PIN is checked in client-side JavaScript, so it is a convenience lock, not real security.
Registrations are not emailed or confirmed anywhere.
Suggested next steps
Add a backend (Flask, FastAPI or Node with Express) and a database (SQLite, PostgreSQL or MongoDB)
Add real authentication with student and admin roles
Send confirmation emails and QR-code tickets for check-in
Export registrations to CSV
Add event images, a calendar view and reminders
Tech stack

HTML5, CSS3 (custom properties, grid, flexbox), vanilla JavaScript (ES6).

License

Free to use and modify for academic and personal projects.# College_Event_Management_System
College_Event_Management_System
