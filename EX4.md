# Ex. No: 4 Creating Procedures using PL/SQL
## DATE:
### AIM: To create a procedure using PL/SQL.

### Steps:
1. Create employee table with following attributes (empid NUMBER, empname VARCHAR(10), dept VARCHAR(10),salary NUMBER);
2. Create a procedure named as insert_employee data.
3. Inside the procdure block, write the query for inserting the values into the employee table.
4. End the procedure.
5. Call the insert_employee data procedure to insert the values into the employee table.
6. Display the employee table

### Program:
``` sql
CREATE TABLE epm(
     empid NUMBER,
     empname VARCHAR(10),
     dept VARCHAR(10),
     salary NUMBER
    );


CREATE OR REPLACE PROCEDURE empe_data AS
    BEGIN
    INSERT INTO epm(empid,empname,dept,salary)
    values(1,'mukil;','CEO',10000000);
    INSERT INTO epm(empid,empname,dept,salary)
    values(2,'sree ram','HR',500000);
    INSERT INTO epm(empid,empname,dept,salary)
    values(3,'sakthi','MD',200000);
    COMMIT;
   FOR empe_rec IN (SELECT * FROM epm)LOOP
   DBMS_OUTPUT.PUT_LINE('EMPLOYEE ID:'||empe_rec.empid||',EMPLOYEE NAME:'|| empe_rec.empname||
   ',DEPARTMENT:'||empe_rec.dept||',SALARY:'||empe_rec.salary);
   END LOOP;
   END;
  /

Begin
    empe_data; end;
    /
```

### Output:

![image](https://github.com/MukeshVelmurugan/Ex-No-4-Creating-Procedures-using-PL-SQL/assets/118707363/c6a8243c-394f-4ca2-8809-4f3f8ff5c7aa)



### Result:
The program has been implemented successfully.
