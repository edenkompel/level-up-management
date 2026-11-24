# LEVEL UP – Studio Management System

A desktop management system for **LEVEL UP**, a fitness studio in Be'er Sheva, built as a group project for the *Systems Analysis & Design* course at Ben-Gurion University. The project covers the full lifecycle: organizational analysis, stakeholder interviews, process modeling, system design and a working implementation.

**Stack:** C# · .NET 8 · WinForms · SQL Server (T-SQL, stored procedures)

Developed with AI-assisted tooling (Claude Code).

## The problem

The studio ran on a split commercial app plus manual work: a whiteboard training plan, WhatsApp reminders and a parallel Excel sheet. The system replaces this with one place to manage trainees, trainers, sessions, rooms, payments and equipment.

## Features

- Trainee and trainer management, registrations and memberships
- Training sessions, room booking and room rental to independent trainers
- Waitlist handling with promotion when a spot opens
- Payments and workout performance tracking
- Equipment and fault reports
- Email notifications and Google Calendar / Tasks API integration
- Manager login

## Project structure

| Path | Contents |
|---|---|
| `LevelUp_Management/` | C# source code (about 11,000 lines), WinForms panels, data classes, services |
| `scripts/` | `create_database.sql` (15 tables), `seed_data.sql`, `stored_procedures.sql` |
| `docs/` | Analysis and design documents: requirements, use cases, BPMN-based organization analysis, class diagram, state diagrams, Part A and Part B reports |

## Analysis and design

- Stakeholder interviews and problem analysis
- Business process modeling (BPMN)
- UML: use cases, class diagram, state diagrams (membership and registration lifecycles)
- Relational schema implemented in SQL Server

## Running locally

1. Create a SQL Server database and run the three scripts in `scripts/`, starting with `create_database.sql`.
2. Copy `LevelUp_Management/App.config.example` to `App.config` and fill in your connection string and SMTP settings.
3. (Optional) Add a Google OAuth `credentials.json` next to the executable to enable Calendar and Tasks integration.
4. Open `LevelUp_Management.sln` in Visual Studio 2022 and run (requires the .NET 8 SDK on Windows).

## Notes

Seed data is fictional. Real credentials are intentionally not included in this repository.
