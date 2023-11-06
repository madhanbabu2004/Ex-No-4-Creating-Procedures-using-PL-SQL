# Ex. No: 4 Creating Procedures using PL/SQL
## DATE:
## AIM: To create a procedure using PL/SQL.

### Steps:
1. Create employee table with following attributes (empid NUMBER, empname VARCHAR(10), dept VARCHAR(10),salary NUMBER);
2. Create a procedure named as insert_employee data.
3. Inside the procdure block, write the query for inserting the values into the employee table.
4. End the procedure.
5. Call the insert_employee data procedure to insert the values into the employee table.
6. Display the employee table

### Program:
```
CREATE TABLE eppplooyeee(
empid NUMBER,
empname VARCHAR(19),
dept VARCHAR(10),
salary NUMBER
);


CREATE OR REPLACE PROCEDURE emp_data AS BEGIN
INSERT INTO eppplooyeee(empid,empname,dept,salary)
values(1, 'BENTEN', 'MANAGER',300000) ;
INSERT INTO eppplooyeee(empid,empname,dept,salary)
values(2, 'KANIS', 'JUNIER' ,640000) ;
INSERT INTO eppplooyeee(empid,empname,dept,salary)
values(3, 'Divya', 'CIVILL',80000000);
COMMIT;

FOR emp_rec IN (SELECT * FROM eppplooyeee)LOOP
DBMS_OUTPUT.PUT_LINE('EMPLOYEE ID:'||emp_rec.empid||',EMPLOYEE NAME:'||emp_rec.empname||
',DEPARTMENT:'||emp_rec.dept||',SALARY:'| |emp_rec.salary);
END LOOP;
END;
/

```
### Output:
![output](./a.png)
![output](./b.png)

### Result:
Thus the procedure has been successfully created in PI/SQL.
