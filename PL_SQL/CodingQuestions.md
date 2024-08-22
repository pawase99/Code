# PLSQL Questioins

**1. Difference between Delete and Truncate?**

                  Delete                                  |                      Truncate
    1. DDL Command                                                       1. DDL Command
    2. Delete is slower                                                  2. Truncate is faster
    3. Rollback is possible after delete statement.                      3. Rollback is not possible after Truncate
    4. wont reclaim the space used.                                      4. reclaim the space used by table
    5. Triggers get invoke                                               5. No triggers invoke.
    6. can use 'where' condition to delete specific rows.                6. Don't use where condition.
    7. Wont reset high level water mark                                  7. Resets high level water mark.
    8. "On delete cascade" from oracle 12c                               8. "Truncate table <table name> cascade" from oracle 12c

**2. Whats difference between Procedure and Function?**

                  Procedure                                |                      Function
    1. Procedure can optionally return value using "Out"                 1.Functions must always return a value.
     & "IN OUT" parameters.
    2. cannot be called from SQL statement.                              2. Function can be called from SQL statement.
      instead **exec procedure_name;**
    3. Used to implement logical data flow.                              3. Function is used for computational purposes.
    4. Procedure can have DML statements.                                4. Functions having DML Statements cannot be called
                                                                            from SQL statements.
                                                                            Autonomous transaction function can be called from SQL statement.
    5. "RETURN" keyword to return out of procedure.                      5. "RETURN" keyword to return the value.
    



                                                                            
