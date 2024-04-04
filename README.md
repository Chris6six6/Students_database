# Students Database Insertion Script

This script inserts data from `courses.csv` and `students.csv` into the "students" database. It also handles the insertion of majors, courses, and their relationships in the database.

## How to Use

1. Ensure that you have the PostgreSQL client installed.
2. Execute the script using `bash insert_data.sh`.
3. The script will truncate the existing data in the tables `students`, `majors`, `courses`, and `majors_courses`.
4. It will then read data from `courses.csv` and `students.csv` to populate the database.

## Script Logic

- The script reads data from `courses.csv` and `students.csv` line by line, separating fields using commas.
- It first checks if the major and course already exist in the database. If not, it inserts them into the respective tables.
- Then, it fetches the IDs of majors and courses to establish the relationships in the `majors_courses` table.
- Finally, it inserts student data into the `students` table, considering majors and their relationships.

## File Structure

- `insert_data.sh`: The main script file responsible for inserting data into the database.
- `courses.csv`: CSV file containing major-course relationships.
- `students.csv`: CSV file containing student data.

## Notes

- Ensure that the PostgreSQL server is running and accessible.
- Modify the script if the CSV file structure or database schema changes.
- Handle errors and edge cases appropriately to ensure data integrity.
- Check the output logs to verify successful insertion of data.
