# PLSQL Questioins

**Difference between Delete and Truncate?**

                  Delete                                  |                      Truncate
    1. DDL Command                                                       1. DML Command
    2. Delete is slower                                                  2. Truncate is faster
    3. Rollback is possible after delete statement.                      3. Rollback is not possible after Truncate
    4. wont reclaim the space used.                                      4. reclaim the space used by table
    5. Triggers get invoke                                               5. No triggers invoke.
    6. can use 'where' condition to delete specific rows.                6. Don't use where condition.
    7. Wont reset high level water mark                                  7. Resets high level water mark.
    8. "On delete cascade" from oracle 12c                               8. "Truncate table <table name> cascade" from oracle 12c
