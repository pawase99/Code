# PLSQL Questioins

**1. Difference between Delete and Truncate?**

                  Delete                                  |                      Truncate
    1. DDL Command                                                     1. DDL Command
    2. Delete is slower                                                2. Truncate is faster
    3. Rollback is possible after delete statement.                    3. Rollback is not possible after Truncate
    4. wont reclaim the space used.                                    4. reclaim the space used by table
    5. Triggers get invoke                                             5. No triggers invoke.
    6. can use 'where' condition to delete specific rows.              6. Don't use where condition.
    7. Wont reset high level water mark                                7. Resets high level water mark.
    8. "On delete cascade" from oracle 12c                             8. "Truncate table <table name> cascade" from oracle 12c

**2. Whats difference between Procedure and Function?**

                  Procedure                                |                      Function
    1. Procedure can optionally return value using "Out"               1.Functions must always return a value.
     & "IN OUT" parameters.
    2. cannot be called from SQL statement.                            2. Function can be called from SQL statement.
      instead **exec procedure_name;**
    3. Used to implement logical data flow.                            3. Function is used for computational purposes.
    4. Procedure can have DML statements.                              4. Functions having DML Statements cannot be called
                                                                          from SQL statements.
                                                                          Autonomous transaction function can be called from SQL statement.
    5. "RETURN" keyword to return out of procedure.                    5. "RETURN" keyword to return the value.

**Can we use DML and DDL inside function?**

https://www.youtube.com/watch?v=yyRM-p2xfZc&list=PLb1qVSx1k1Vr0v4wVyvT3GEuA0J0M4xBm&index=13
    

**3. Explain PL/SQL execution Architecture**

  Client server architecture

  The transfer
  
  sends them to the sql statement processor

**4. What virtual tables are accessible during database trigger is running?**

  The virtual columns that are accessible during the database triggers execution are THEN and NOW tables. THEN.column and NOW.column are the names of respective tables columns.

  The only allowed column for insert related triggers is NOW.column

  The only allowed column for delete related triggers is THEN.column.

  Upadte can be performed on both THEN and NOW tables.

**5. What distinguishes ROLLBACK and ROLLBACK TO statement in PL-SQL**

  ROLLBACK command is used to undo any modification made since the transactions start

  ROLLBACK TO is used to ROLLBACK upto SAVEPOINT.

**6. What component make up to a PLSQL package?**

**7. Benefits of PLSQL package?**

   -Enforced information hiding
   -top down create
   -object perstence
   -object oriented design
   -transaction integrity guaranteed
   -performance enhancement

**8. What is exception Handling?**

  Runtime errors are handled by a process called exception handling.

  User defined exception
  System defined exception

**9. How can your plsql code be debugged?**

  to debug our code, we can use the DBMS_OUTPUT and DBMS_DEBUG statements.
  DBMS_DEBUG is used to print the output to a logfile.

**10. What distinguishes mutating trigger with constraining tables?**

  Currently a table that is being changed through the use of DML Statement is referred as mutating.

  constraining table is one that is read for the purpose of restricting referential integrity.

****

  
