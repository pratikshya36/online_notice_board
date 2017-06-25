# online_notice_board
use github issues to host images
### CODE FOR CREATING ADMIN:
CREATE USER 'prof_admin'@'localhost' IDENTIFIED BY 'prof1234'; 
GRANT ALL PRIVILEGES ON md5_password.* TO 'prof_admin'@'localhost' 
WITH GRANT OPTION; FLUSH PRIVILAGES;

### DATABASE INCLUDED:
## md5_password 
## TABLES included: 
# 1.student_registration:
To store the students(non-admins). It contains 3 fields:id(auto-incremented),student_id,password
![student_registration](https://user-images.githubusercontent.com/28576445/27514738-1985ed2a-59b1-11e7-8ad9-d20221d4f907.PNG)

# 2.admins_registration:
To store the admins.(The original admin is also included in this table). It contains 3 fields:id(auto-incremented),username,password

# 3.student_notes:
To store the notes. It contains 3 fields:id(auto-incremented),subject,notes       
