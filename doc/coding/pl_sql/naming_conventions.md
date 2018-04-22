[Development Guidelines](../../../README.md) / [Coding](../../../README.md#coding) / [PL/SQL](../../../README.md#coding_pl_sql)

## [Naming Conventions](../../../README.md#coding_pl_sql_naming_conventions)

### File Names

File Type | Extension
:--------- | :---------:
Package body | pkb
Package (or package specification) | pks
Function | fnc
Procedure | prc
Trigger | trg
Object type body | tpb
Object type (or object type specification) | tps
Any other PL/SQL | pls
Any other SQL | sql

----

### Identifier Names

**Must**

- **Invoke** functions and procedures without any arguments with `()`.
- Add **labels** to the `END` statements of all your packages, procedures, functions etc.
- The total **length** of an identifier name is limited to 30 characters.
- Make **plural** anything that contains multiple pieces of information, that aree mainly relational tables and collections. 
- - **Qualify** all column names and variable names inside SQL in PL/SQL.
- The **root name** of the identifier is the part of the identifier name that describes concisely and accurately the meaning of the thing named.
- The **scope prefix** (SC) is either `g_` for global, `l_` for local or `p_` for parameters.
- **Upper-case** non-application identifiers (elements of the PL/SQL and SQL language and Oracle built-ins) and **lower-case** application specific elements.

----

**Avoid**

- Using names like `i` and `j`.
- Including an indicator of the **datatype** in the name, as in `g_i_counter`.
- Using names defined in the `STANDARD` and `DBMS_STANDARD` **packages**.
- **Recycling** names.
- **Repeating** names at different scopes.
- **Starting** your procedures with `p_` / `sp_` or functions with `f_` / `sf_`.
 
---- 

Naming convention | Type of identifier | Example 
:---------------- | :----------------- | -------          
`c_rootname`       | constant declared in a PL/SQL block | `c_max_salary` 
`e_rootname`       | exception | `e_balance_too_low` 
`en_rootname`      | exception number (a constant that is assigned the value of an error code)                              | `en_balance_too_low CONSTANT PLS_INTEGER = -20555` 
`g_rootname`       | variable declared at the package level | `g_total_sales` 
`gc_rootname`      | constant declared at the package level | `gc_max_salary` 
`l_rootname`       | variable declared in a PL/SQL block | `l_total_sales` 
`p_rootname_in`    | `IN` parameter | `p_salary_in` 
`p_rootname_inout` | `IN OUT` parameter | `p_salary_inout` 
`p_rootname_out`   | `OUT` parameter | `p_salary_out` 
`SC_rootname_aat`  | associative array collection | `l_employees_aat` 
`SC_rootname_aatv` | associative array collection variable | `l_employees_aatv` 
`SC_rootname_cur`  | explicit cursor | `l_employees_cur` 
`SC_rootname_cv`   | cursor variable | `l_name_and_salary_cv` 
`SC_rootname_nt`   | nested table collection | `l_employees_nt` 
`SC_rootname_ntv`  | nested table collection vriable | `l_employees_ntv` 
`SC_rootname_ot`   | object type | `l_employee_ot` 
`SC_rootname_rt`   | record type | `l_name_and_salary_rt` 
`SC_rootname_rtv`  | record variable | `l_employee_rtv` 
`SC_rootname_vat`  | `VARRAY` collection | `l_employees_vat`
`SC_rootname_vatv` | `VARRAY` collection variable | `l_employees_vatv`