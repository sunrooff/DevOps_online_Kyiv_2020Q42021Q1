# Module 3 Database Administration.
## TASK 3.1
### PART 1

1. MySQL server veriosn after downloading :</br></br>
![1](./screenshots/1.png)</br>


2. **(2-5 tasks)**. MySQL server is installed. Database was created on the server through the console and filled :</br></br>
  ![1](./screenshots/4-5.png)</br></br>
  ![1](./screenshots/4.png)</br>


6. Operators that I used.</br></br>
  WHERE :</br>
  ![1](./screenshots/6.png)</br></br>
  GROUP BY :</br>
  ![1](./screenshots/6.2.png)</br></br>
  OERDER BY :</br>
  ![1](./screenshots/6.1.png)</br></br>

7. SQL queries that I used :</br></br>
   **DDL (data definition language) -> create, alter, drop :**</br>
   ![1](./screenshots/7.1.1.png)</br></br>
   ![1](./screenshots/7.1.2.png)</br></br>
   ![1](./screenshots/7.1.3.png)</br></br>

   **DML (data manipulation language) -> select, insert, update :**</br>
   ![1](./screenshots/7.2.1.png)</br></br>
   ![1](./screenshots/7.2.1.png)</br></br>
   ![1](./screenshots/7.2.3.png)</br></br>


   **DCL (data control language) -> grant, revoke :**</br>
   ![1](./screenshots/7.3.1.png)</br></br>
   ![1](./screenshots/7.3.2.png)</br>


8. Created new user and connected to the database with all privileges.</br>
  ![1](./screenshots/8.1.png)</br></br>
  ![1](./screenshots/8.2.png)</br></br>


9. Make a selection from the main table DB MySQL.</br>
   **TBD**

### PART 2

10. Backup of database is done using the next CL :</br>
    -*sudo mysqldump sunroof_DB > backup_sunroof_DB.sql*</br></br>
    ![1](./screenshots/10.png)</br>


11. Table and database were deleted using the next CL :</br>
    - *drop table workers_DB;*
    - *drop database sunroof_DB;*


12. Database is restored using the next CL :</br>
    - *sudo mysql new_sunroof_DB < backup_sunroof_DB.sql*</br>


13. Transfer of local database to RDS AWS.</br>
![1](./screenshots/13.1.png)</br></br>
Transfer :</br>
![1](./screenshots/13.2.png)</br></br>

14. Connect to database RDS AWS :</br>
![1](./screenshots/13.3.png)</br>
15. Executed SELECT operator WHERE :</br>
![1](./screenshots/13.4.png)</br>

16. Dump is created from RDS AWS :</br>
![1](./screenshots/13.5.png)</br>


### PART 3</br></br>

17. Amazon DynamoDB table is created :</br>
![1](./screenshots/17.png)</br></br>

18. Enter data into an Amazon DynamoDB table.</br>
![1](./screenshots/18.1.png)</br></br>

19. Amazon DynamoDB table is filtered using query and scan.</br>
  **Scan :**</br>
  ![1](./screenshots/19.png)</br></br>
  **Query :**</br>
  ![1](./screenshots/19.1.png)</br>
