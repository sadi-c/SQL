# SQL Example

## Example Tables
1. **students**
   | id  | name      | age | gender |
   | --- | --------- | --- | ------ |
   | 1   | Alice     | 18  | Female |
   | 2   | Bob       | 20  | Male   |
   | 3   | Charlie   | 19  | Male   |

2. **courses**
   | id  | name            | credits |
   | --- | --------------- | ------- |
   | 1   | Math            | 3       |
   | 2   | Science         | 4       |
   | 3   | English         | 3       |

3. **enrollments**
   | id  | student_id | course_id | grade |
   | --- | ---------- | --------- | ----- |
   | 1   | 1          | 1         | A     |
   | 2   | 2          | 2         | B     |
   | 3   | 3          | 1         | C     |

## SQL Query Example
Let's write a query to find the name and grade of all students who are enrolled in the Math course.

```
SELECT 
    students.name AS student_name, 
    enrollments.grade
FROM 
    students
JOIN 
    enrollments ON students.id = enrollments.student_id
JOIN 
    courses ON enrollments.course_id = courses.id
WHERE 
    courses.name = 'Math'; 

```

SELECT: Specifies the columns name from the students table and grade from the enrollments table.
FROM: Indicates the primary table students to start the query.
JOIN: Combines rows from the students, enrollments, and courses tables based on the related columns (students.id = enrollments.student_id and enrollments.course_id = courses.id).
ON: Specifies the conditions for the joins.
WHERE: Filters the results to include only those students who are enrolled in the Math course.
