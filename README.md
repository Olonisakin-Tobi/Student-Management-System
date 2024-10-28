# Student-Management
                                     -- QUESTION 1
-- Database Creation & Schema Design
create database school_management;

-- Student:
create table students(
student_id int PRIMARY KEY,
First_name VARCHAR(50),
Last_name VARCHAR(50),
dob DATE,
Email VARCHAR(50),
Phone_number VARCHAR(20)
);

-- COURSES:
CREATE TABLE courses(
Course_id INT PRIMARY KEY,
Course_name VARCHAR(50),
Course_code VARCHAR(25),
credits INT
);

-- ENROLLMENT:
CREATE TABLE enrollments(
Enrollment_id INT PRIMARY KEY,
student_id INT,
course_id INT,
enrollment_date DATE
);

-- GRADE
CREATE TABLE grade(
Grade_id INT PRIMARY KEY,
Enrollment_id INT,
Grade VARCHAR(5)
);

                     -- QUESTION 2:Alterations and Modificatio
-- Add a column `address` to the `students` table

ALTER TABLE students ADD COLUMN address VARCHAR(100);

-- Modify the `course_name` column in the `courses` table to be of type `VARCHAR(100)`
 
 ALTER TABLE courses MODIFY COLUMN Course_name VARCHAR(100);
 
 -- Change the position of the `credits` column to be right after the `course_code` in the `courses` table
 
 ALTER TABLE courses MODIFY COLUMN credits VARCHAR(25) AFTER Course_code;
 
 -- Rename the `dob` column in `students` to `date_of_birth

 ALTER TABLE students RENAME COLUMN dob TO date_of_birth;
 
 
                             -- QUESTION 3 Data Insertion
-- Insert at least 30 students into the `students` table.
INSERT INTO students(student_id, First_name, Last_name, date_of_birth, Email, Phone_number, address) VALUES
(1,'Olonisakin','Emmanuel','2002-12-12','emmanuelk5@gmail.com','08183691814','phase 1 site 1 pw kubwa'),
(2,'Olaoluwa', 'Faith', '1997-10-10', 'faitho@gmail.com', '09029458321', 'blk 2 flt 2 fo1 kubwa'),
(3, 'Akinde', 'Happiness', '1999-08-13','Akindeh@gmail.com', '08049385763', '44 john street'),
(4, 'Fabunmi', 'praise', '1990-01-10', 'fabunmip@gmail.com', '09039299570', '23 hamilton street'),
(5, 'Ajiboye', 'faith', '2003-02-10', 'ajiboyef2gmail.com', '09063286754','Akin street 31'),
(6, 'Frank', 'Wilson', '2005-06-10', 'frankwilson@gmail.com',0903245673,'2 wasabi street'),
(7, 'Grace', 'Carter', '2006-07-15', 'gracecarter@gmail.com', '08039284039', '34 sandral close'),
(8, 'Henry', 'Miller', '2007-08-20', 'henrymiller@gmail.com', '09047589382','89 chika street'),
(9, 'Isabella', 'Taylor', '2008-09-25', 'isabellataylor@gmail.com', '09029847503','23 sunvill estate'),
(10, 'Jack', 'Harris', '2009-10-30', 'jackharris@gmai.com', '09068932958','arab road'),
(11, 'Kate', 'Jones', '2010-11-05', 'katejones@gmai.com', '08034958432', '23 isak road'),
(12, 'Liam', 'Martin', '2011-12-10', 'liammartin@gmai.com', '08055179669','1600 Ash St, Here'),
(13, 'Maya', 'Garcia', '2012-01-15', 'mayagarcia@gmai.com', '09123498576','1500 Birch St, Overthere'),
(14, 'Noah', 'Baker', '2013-02-20', 'noahbaker@gmai.com', '09049302943','1400 Chestnut St, Somewhere'),
(15, 'Olivia', 'Allen', '2014-03-25', 'oliviaallen@gmai.com', '09049380984','1300 Cedar St, Anywhere'),
(16, 'Paul', 'Carter', '2015-04-30', 'paulcarter@gmai.com', '09059485321','1200 Willow St, Wherever'),
(17, 'Quinn', 'Davis', '2016-05-05', 'quinndavis@gmai.com', '09089756432','1100 Maple St, There'),
(18, 'Riley', 'Wilson', '2017-06-10', 'rileywilson@gmai.com', '08095843219','1000 Oak St, Here'),
(19, 'Sophia', 'Carter', '2018-07-15', 'sophiacarter@gmai.com', '09084738490','909 Sycamore St, Overthere'),
(20, 'Thomas', 'Miller', '2019-08-20', 'thomasmiller@gmai.com', '09085743285','808 Alder St, Somewhere'),
(21, 'Uma', 'Taylor', '2020-09-25', 'umataylor@gmai.com', '08127348573','707 Ash St, Anywhere'),
(22, 'Vincent', 'Harris', '2021-10-30', 'vincentharris@gmai.com', '09083948593', '606 Birch St, Wherever'),
(23, 'Willow', 'Jones', '2022-11-05', 'willowjones@gmai.com', '08129384509', '505 Chestnut St, There'),
(24, 'Xavier', 'Martin', '2023-12-10', 'xaviermartin@gmai.com', '09039485634','404 Cedar St, Here'),
(25, 'Yara', 'Garcia', '2024-01-15', 'yaragarcia@gmai.com', '08139485675','303 Willow St, Overthere'),
(26, 'Zachary', 'Baker', '2025-02-20', 'zacharybaker@gmai.com', '09029385793','202 Maple St, Somewhere'),
(27, 'Abigail', 'Allen', '2026-03-25', 'abigailallen@gmai.com', '081942209584','101 Elm St, Anywhere'),
(28, 'Benjamin', 'Carter', '2027-04-30', 'benjamincarter@gmai.com', '08120948357','789 Pine St, Othertown'),
(29, 'Chloe', 'Davis', '2028-05-05', 'chloedavis@gmai.com', '08029389342','456 Oak Ave, Somecity'),
(30, 'Daniel', 'Wilson', '2029-06-10', 'danielwilson@gmai.com', '09039847209','123 Main St, Anytown');

-- Insert at least 10 courses into the `courses` table
INSERT INTO courses (course_id, course_name, course_code, credits) VALUES
(1, 'Mathematics', 'MATH101', 3),
(2, 'English', 'ENG101', 3),
(3, 'Science', 'SCI102', 4),
(4, 'fluid mech', 'ENG201', 2),
(5, 'Highway engineering', 'ENG301', 3),
(6, 'Computer Science', 'CS411', 4),
(7, 'data analysis', 'DT301', 6),
(8, 'Music', 'MUS501', 2),
(9, 'Education', 'EDU400', 2),
(10, 'Language', 'LAN203', 1);

-- Insert at least 12 records into the `enrollments` table, ensuring that some students are enrolled in multiple courses.
INSERT INTO enrollments (enrollment_id, student_id, course_id, enrollment_date)
VALUES
  (1, 1, 1, '2023-09-01'),
  (2, 2, 1, '2023-09-01'),
  (3, 3, 2, '2023-09-01'),
  (4, 4, 3, '2023-09-01'),
  (5, 1, 2, '2023-09-02'),
  (6, 2, 3, '2023-09-02'),
  (7, 5, 1, '2023-09-03'),
  (8, 6, 2, '2023-09-03'),
  (9, 7, 3, '2023-09-04'),
  (10, 8, 1, '2023-09-04'),
  (11, 9, 2, '2023-09-05'),
  (12, 10, 3, '2023-09-05');

INSERT INTO grade(grade_id, enrollment_id, grade) VALUES
(90, 1, 'A'),
(80, 2, 'B'),
(70, 3, 'C'),
(60, 4, 'D'),
(50, 5, 'F'),
(72, 6, 'C'),
(82, 7, 'B'),
(76, 8, 'C'),
(65, 9, 'D'),
(57, 10, 'F'),
(92, 11, 'A'),
(5, 12, 'F');
SElECT * FROM enrollments;
SElECT * FROM students;
SELECT * FROM courses;
SELECT * FROM grade;

                                         -- QUESTION 4: Complex Queries
-- Write a query to retrieve the full names and courses for all students.

SELECT s.student_id, CONCAT(s.first_name, '-', s.last_name) AS full_name,c.Course_name
FROM students AS s
JOIN enrollments AS e
ON s.student_id = e.student_id
JOIN courses AS c
ON e.Course_id = c.Course_id;

-- Write a query to find all students who have not yet been assigned a grade

SELECT students.student_id, CONCAT(students.first_name, '-', students.last_name) AS full_name
FROM students
left JOIN enrollments 
ON students.student_id = enrollments.student_id
left JOIN grade
 ON enrollments.enrollment_id = grade.enrollment_id
WHERE grade.grade_id IS NULL;

--  Write a query that returns the average grade for each course

SELECT courses.course_name, AVG(grade.grade) AS average_grade
FROM courses
JOIN enrollments ON courses.course_id = enrollments.course_id
JOIN grade ON enrollments.enrollment_id = grade.enrollment_id
GROUP BY courses.course_id;


-- Create a `CASE` statement to assign letter grades (A, B, C, D, F) based on numerical grades.

SELECT grade.Enrollment_id,Grade_id, courses.course_name,grade.grade,
  CASE
    WHEN grade.Grade_id >= 90 AND grade.Grade_id <= 100 THEN 'A'
    WHEN grade.Grade_id >= 80 AND grade.Grade_id <= 89 THEN 'B'
    WHEN grade.Grade_id >= 70 AND grade.Grade_id <= 79 THEN 'C'
    WHEN grade.Grade_id >= 60 AND grade.Grade_id <= 69 THEN 'D'
    ELSE 'F'
  END AS letter_grade
FROM courses
JOIN enrollments 
ON courses.course_id = enrollments.course_id
JOIN grade 
ON enrollments.enrollment_id = grade.enrollment_id;

-- Use subqueries to find students with the highest grades in each course

SELECT courses.course_name, students.first_name, students.last_name, MAX(grade.grade_id) AS highest_grade
FROM courses
JOIN enrollments 
ON courses.course_id = enrollments.course_id
JOIN grade
 ON enrollments.enrollment_id = grade.enrollment_id
JOIN students
 ON enrollments.student_id = students.student_id
GROUP BY grade.grade_id
order by highest_grade DESC
LIMIT 1;

SELECT * FROM students;
select * from courses;
Select * from grade;
select * FROM enrollments;

                         -- QUESTION 5:Using CTEs (Common Table Expressions)
-- Write a CTE to list all students with their course names and grades

WITH StudentCourseGrades AS (
  SELECT concat(s.first_name,'-',s.last_name) AS full_name, c.course_name,g.grade
  FROM students s
  JOIN enrollments e 
  ON s.student_id = e.student_id
  JOIN courses c
  ON e.course_id = c.course_id
  JOIN grade g 
  ON e.enrollment_id = g.enrollment_id
)
SELECT * FROM StudentCourseGrades;


-- Write a CTE to find students who have taken more than 2 courses.

WITH StudentCourseCounts AS (
  SELECT student_id, COUNT(*) AS num_courses
  FROM enrollments
  GROUP BY student_id
)
SELECT CONCAT(s.first_name,'-',s.last_name) AS full_name,s.student_id,c.num_courses
FROM students s
JOIN StudentCourseCounts c
ON s.student_id = c.student_id
WHERE c.num_courses >= 2;

                                         -- QUESTION 7: Additional Tasks

-- Write a query to count the number of students enrolled in each course.

SELECT courses.course_name, COUNT(enrollments.student_id) AS enrolled_students
FROM courses
JOIN enrollments ON courses.course_id = enrollments.course_id
GROUP BY courses.course_name;

-- Create a report showing the total number of students, courses, and enrollments.

SELECT
  (SELECT COUNT(*) FROM students) AS total_students,
  (SELECT COUNT(*) FROM courses) AS total_courses,
  (SELECT COUNT(*) FROM enrollments) AS total_enrollments;
  
-- Use a JOIN to retrieve the names of students and the courses they are not enrolled in.

SELECT students.first_name, students.last_name, courses.course_name
FROM students
CROSS JOIN courses
LEFT JOIN enrollments ON students.student_id = enrollments.student_id
  AND courses.course_id = enrollments.course_id
WHERE enrollments.enrollment_id is null;

-- Write a query to find students who share the same last name.

SELECT last_name, COUNT(*) AS count
FROM students
GROUP BY last_name
HAVING COUNT(*) > 1;

-- Delete all records from the grades table where the grade is below 50 and record the number of rows deleted.
DELETE FROM grades
WHERE grade < 50;

SELECT ROW_COUNT() AS deleted_rows;
