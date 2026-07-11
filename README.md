# Student Database Importer

A Bash automation project that imports student, major, and course data from CSV files into a PostgreSQL database.

## Overview

This project demonstrates how to automate database population using Bash scripting and SQL. The script creates majors, courses, relationships, and student records while preventing duplicate entries and preserving referential integrity.

## Features

- Import data from CSV files
- Automatically create missing majors and courses
- Populate many-to-many relationships
- Handle NULL values for undeclared majors
- Reset the database before each import
- Prevent duplicate data insertion

## Database Design

Tables:

- students
- majors
- courses
- majors_courses

Relationships:

- One major can have many students.
- A major can include many courses.
- A course can belong to multiple majors.

## Technologies

- Bash
- PostgreSQL
- SQL
- CSV

## Files

| File | Purpose |
|------|---------|
| insert_data.sh | Imports CSV data into PostgreSQL |
| students.sql | Database schema and tables |
| courses.csv | Major-course mapping |
| students.csv | Student records |

## How to Run

Clone the repository:

```bash
git clone https://github.com/yourusername/student-database-importer.git
cd student-database-importer
```

Restore the database:

```bash
psql -U freecodecamp < students.sql
```

Run the importer:

```bash
bash insert_data.sh
```

## Skills Demonstrated

- Bash scripting
- SQL
- PostgreSQL
- Database normalization
- Primary and foreign keys
- Many-to-many relationships
- CSV parsing
- Data automation

## Future Improvements

- Command-line arguments
- Logging
- Error handling
- Docker support
- Unit tests

## License

MIT License
