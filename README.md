# online_notice_board
use github issues to host images
## SOFTWARE USED
WAMP 
## EDITOR USED:
NOTEPAD++
## BROWSER USED:
GOOGLE CHROME

### CODE FOR CREATING ADMIN:
CREATE USER 'prof_admin'@'localhost' IDENTIFIED BY 'prof1234'; 
GRANT ALL PRIVILEGES ON md5_password.* TO 'prof_admin'@'localhost' 
WITH GRANT OPTION; FLUSH PRIVILAGES;

### DATABASE INCLUDED:
## md5_password 
![database](https://user-images.githubusercontent.com/28576445/27514796-6d589e92-59b2-11e7-915b-dfc2b5e0cca5.PNG)
## TABLES included: 
# 1.student_registration:
To store the students(non-admins). It contains 3 fields:id(auto-incremented),student_id,password
![student_registration](https://user-images.githubusercontent.com/28576445/27514738-1985ed2a-59b1-11e7-8ad9-d20221d4f907.PNG)

# 2.admins_registration:
To store the admins.(The original admin is also included in this table). It contains 3 fields:id(auto-incremented),username,password
![admin_registration](https://user-images.githubusercontent.com/28576445/27514798-7877d5a4-59b2-11e7-8762-619bb4a5d012.PNG)

# 3.student_notes:
To store the notes. It contains 3 fields:id(auto-incremented),subject,notes 
![student_notes](https://user-images.githubusercontent.com/28576445/27514800-7f513ea6-59b2-11e7-8e84-b2e1d0b32885.PNG)

### MORE DETAILS ABOUT THE TASK
# CONNECTION TO DATABASE:
  used SQL query: mysqli_connect("localhost","prof_admin","prof1234","md5_password);
  
# 1.FIRST CREATED REGISTRATION PAGE:
  It asks for the studentid and password and stores the information in student_registration table.There are 3 labels:STUDENT      ID,PASSWORD,RETYPE PASSWORD.It displays alert message either when any field is empty or when passwords don't match.
  Password is encrypted using base64_encode() so that it can be decrypted when required.Already registered students are directed to       login page.
  
# 2.THEN CREATED LOGIN PAGE:
Already registered users can login.It asks whether you are professor(admin) or student.The admin can log in using username and        password.If entries are incorrect it displays an alert message.Otherwise the user is directed to bulletin bard page.
