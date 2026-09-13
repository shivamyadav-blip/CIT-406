## Test 1: Student Without a First Name

I tested the NOT NULL constraint on the `first_name` column by running the following statement:

```sql
INSERT INTO club_members
    (last_name, email, major, join_date)
VALUES
    ('Williams', 'williams@university.edu', 'Cybersecurity', '2026-09-06');
```

### PostgreSQL Error

```text
ERROR: null value in column "first_name" of relation "club_members" violates not-null constraint
Failing row contains (6, null, Williams, williams@university.edu, Cybersecurity, 2026-09-06).

SQL state: 23502
Detail: Failing row contains (6, null, Williams, williams@university.edu, Cybersecurity, 2026-09-06).
```

### Explanation

PostgreSQL rejected this row because I did not provide a value for `first_name`. I defined the `first_name` column with a NOT NULL constraint, so PostgreSQL does not allow a club member to be inserted without a first name.

## Test 2: Student Without an Email Address

I tested the NOT NULL constraint on the `email` column by running the following statement:

```sql
INSERT INTO club_members
    (first_name, last_name, major, join_date)
VALUES
    ('Olivia', 'Brown', 'Information Technology', '2026-09-07');
```

### PostgreSQL Error

```text
ERROR: null value in column "email" of relation "club_members" violates not-null constraint
Failing row contains (7, Olivia, Brown, null, Information Technology, 2026-09-07).

SQL state: 23502
Detail: Failing row contains (7, Olivia, Brown, null, Information Technology, 2026-09-07).
```

### Explanation

PostgreSQL rejected this row because I left out the `email` value. Since I defined the `email` column with a NOT NULL constraint, every club member must have an email address before the row can be inserted.

## Result
