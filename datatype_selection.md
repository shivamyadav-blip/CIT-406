| # | Column | PostgreSQL Data Type | Justification |
|---|--------|----------------------|---------------|
| 1 | student_id | INTEGER GENERATED ALWAYS AS IDENTITY | I chose an identity integer because PostgreSQL can automatically generate a new numeric ID for each student. |
| 2 | first_name | VARCHAR(50) | I chose VARCHAR(50) because student first names are generally shorter than 50 characters. |
| 3 | email_address | VARCHAR(255) | I chose VARCHAR(255) because an email address is text and its length can vary. |
| 4 | date_of_birth | DATE | I chose DATE because only the student's birth date is needed and no time information is required. |
| 5 | account_balance | NUMERIC(10,2) | I chose NUMERIC(10,2) because account balances can contain dollars and cents and should be stored precisely. |
| 6 | is_active | BOOLEAN | I chose BOOLEAN because the account has only two possible states, active or inactive. |
| 7 | event_start | TIMESTAMPTZ | I chose TIMESTAMPTZ because the event has an exact date and time and students may participate from different time zones. |
| 8 | event_description | TEXT | I chose TEXT because an event description may contain several paragraphs and does not have a fixed maximum length. |
| 9 | maximum_attendees | INTEGER | I chose INTEGER because the maximum number of attendees is a whole number. |
| 10 | student_attended | BOOLEAN | I chose BOOLEAN because attendance can be represented with two states, yes or no. |
| 11 | phone_number | VARCHAR(25) | I chose VARCHAR(25) because phone numbers can contain characters such as plus signs, spaces, parentheses, and hyphens. |
| 12 | postal_code | VARCHAR(10) | I chose VARCHAR(10) because postal codes should be treated as text so values such as leading zeros can be preserved. |
| 13 | event_status | VARCHAR(20) | I chose VARCHAR(20) because it can store statuses such as scheduled, cancelled, or completed while allowing other statuses later. |
| 14 | student_number | VARCHAR(6) | I chose VARCHAR(6) because the student number contains leading zeros that need to be preserved. |
