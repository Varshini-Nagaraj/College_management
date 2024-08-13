1.SELECT s.student_id, s.name,s.course,f.fee_id, f.amount, f.due_date, f.status 
 FROM 
 Fees f JOIN Students s 
 ON f.student_id = s.student_id
 WHERE f.status = 'unpaid';
![C1](https://github.com/user-attachments/assets/631f5a9d-bdc3-4e5e-8364-5792881face4)


2.SELECT 
    s.course,
    COUNT(s.student_id) AS student_count,
    MAX(a.status) AS status
FROM 
    Attendance a 
JOIN   
    Students s 
ON 
    a.student_id = s.student_id 
WHERE 
    a.status = 'Absent'
GROUP BY  
    s.course
LIMIT 0, 1000;
![C2](https://github.com/user-attachments/assets/2de1731e-3c5e-4545-b704-42307bcfbee0)

