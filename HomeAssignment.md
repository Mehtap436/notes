Mehtap Kirsan 
Q1
SELECT * FROM rectangles;
Q2
SELECT COUNT(*) AS rectangle_count FROM rectangles;
Q3
SELECT color FROM rectangles ORDER BY width DESC LIMIT 1;
Q4
SELECT color FROM rectangles ORDER BY height DESC LIMIT 1;
Q5
SELECT * FROM rectangles WHERE width > height;
Q6
SELECT id, width, height, width * height AS Area FROM rectangles;
Q7
SELECT color FROM rectangles ORDER BY (width * height) DESC LIMIT 1;
Q8
SELECT color FROM rectangles ORDER BY (x + width) DESC LIMIT 1;
Q9
SELECT * FROM rectangles WHERE color IS NULL;
Q10
SELECT DISTINCT color FROM rectangles;
Q11
SELECT DISTINCT color FROM rectangles WHERE color IS NOT NULL AND color NOT LIKE '#%';
Q12
SELECT UPPER(color) AS color_uppercase FROM rectangles;
Q13
SELECT course_id FROM courses ORDER BY LENGTH(course_name) DESC LIMIT 1;
Q14
SELECT COUNT(*) AS assignment_count FROM assignments WHERE due_date LIKE '2024%';
Q15
SELECT course_id || ': ' || course_name AS course_info FROM courses;
Q16
SELECT course_id, course_name, lab_time FROM courses WHERE lab_time LIKE 'Monday%';
Q17
SELECT * FROM assignments WHERE due_date < DATE('now');
Q18
SELECT course_id, COUNT(*) AS assignment_count FROM assignments GROUP BY course_id;
BONUS Q1
SELECT semester, COUNT(*) AS assignment_count FROM courses 
JOIN assignments ON courses.course_id = assignments.course_id 
GROUP BY semester;
BONUS Q2
SELECT id, color, SUBSTR(color, 2, 2) AS red_component 
FROM rectangles 
WHERE color LIKE '#%';