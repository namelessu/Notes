### DB Life Cycle
1. Analysis->System analyst: Gathering information and writing the business and requirement document.
2. DB Design->ERD(Entity Relational Diagram):It can be different from the view of someone to other.
3. DB Mapping->Designing the schema, Setting Rules and constraints, Creating the tables: It is impossible to have two schema conflicting with each other and in this case the business requirement document should be revised.
4. DB implementation: SQL(Structure Query Language) implementation using the RDBMS(Relational Database Management Studio) tool such as MYSQL,Oracle,Access, etc.
5. Client->End User->Browser->URL: So the user can use a simple interface with the application.
### File Base system vs the Database system.

| File Base system                                               |
| -------------------------------------------------------------- |
| Delimited File: Data is seprated by a delimiter such as comma. |
| Fixed Width File: Data are all stored in same byte size        |
**Disadvantages of File based system:-**

1. Search Difficulty
2. Duplicate data is possible.
3. No constraints or rules
4. No data quality
5. Manual backup and restore.
6. Separated copies.
7. Lack Of integrity and security.
8. Long Development Time.
---

| Database                                                   |
| ---------------------------------------------------------- |
| Collection of related data that has constraints and rules. |
**Advantages of Database**
1. Relationship and constraints.
2. Security and integrity.
3. No Duplicate data.
4. Sharing Data.
5. Redundancy and Backup
### ERD notations And Logic
**notations**
- Rectangles: Entities
- Ellipses:Attributes
- Diamonds:Relationship
**Entity type**
- Strong Entity: An entity that has primary key so if it is deleted the child is not deleted.
- Weak Entity: An entity that is deleted when the parent is deleted for example if account data is deleted the transactions he did is also deleted.
**Attribute types**
1. Simple attribute: Normal Ellipse
	- Cannot be calculated in the runtime.
	- Cannot be divided into different attributes(Not Composite).
	- Cannot be multiple attribute(No multiple data of the same type)
2. Multi-Valued Attribute: Double Ellipse
	- Multiple Data of the same type for example multiple address of employee, multiple phone numbers, etc.
3. Derived Attribute: Dotted Ellipse
	- Calculated based on an equation or a relation for example the net salary of employee
4. Composite Attribute
	- An attribute that can be divided into multiple attributes for example the name of employee consists of first name and second name.
5. Complex Attribute: Composite and multi-valued in the same time.
### Relationships
1. Degree of Relation ship
	1. Unary
	2. Binary
	3. Ternary
2. Cardinality
	- One To One: For example each student has one and single ID
	- One To Many: For example Each department has many employees
	- Many To Many:For example Many courses has many students
3. Participation Constraint
	- Total participation: When the side of the entity must participate in the relationship it is total participation and notated by 2 line for example and employee must be hired by a department.
	- Partial participation: When the side of entity is optionally participating it is partial participation and notate by one line example: a department may hire employee
---
### Types of keys
1. Candidate key: Any key that is possibly be chosen as a primary key.
2. Primary key: Any key that is unique and not null.
3. Composite key: A key consist of two or multiple metadata for example lets say that the employee has name and address if both are chosen and generate a unique and not null key it is a composite primary key.
4. Foreign key: That defines relationship.
---
### Database mapping and schema design steps
1. Strong entity:
	- If there is strong entity i create table for it having it is primary key and attributes, In case i got derived attribute i don't create a column for it as i can just put it in constraint table, If i got multi-valued attribute i create a new table with foreign key aiming at the primary key of the original table and the primary key becomes a composite key consisting of all the attributes i got in the new table, If i got composite attribute i take it's content and put it as a columns and i write a notice in constrain document.
2. Weak entity:
	- If there is a weak entity i create a new table with composite primary key consisting of the partial key of the weak entity and the foreign key that aims at the primary key of the strong entity.
3. Cardinality In case of binary relation ship:
	- If i got a relationship 1:1 total participation from the two sides, I create a table consisting of primary key of either entities and a foreign key from one entity aiming the primary key of the other.  
	- If i got a relationship 1:1 total participation from a side and another optional participation i create 2 tables, the first table of the entity that totally participate shall have the primary key and the other that optionally participate shall have it is primary key and foreign key aiming at the the primary key of the other table.
	- if i got 1:1 relationship and partial participation from the 2 sides i create a new table with 2 foreign keys aiming at both primary keys of the 2 tables i already created and either one is allowed to act as a primary key.
	- 1:M relationship with total participation from the side of M and the 1 side optionally participate i create 2 tables the one that optionally participate side has it is own table with foreign key aiming at the primary key of the other
	- 1:M relationship with partial participation from the two sides i take the foreign key in the table of the 1 side aiming at the primary key of the M side attribute table.
	- In case or M:M relationship i don't look at the carnality and i create a new table with two foreign keys aiming at both primary keys of the original two tables and the primary key becomes a composite primary key consisting of both.
4. Ternary and higher degrees relationships:-
	- I create all tables as known and a new table containing the relation attributes and foreign key aiming at the tables primary key i created, then i check which combination can make a composite primary key.
5. Self relationship:
	- i create a table with primary and foreign key and the foreign key aims at the primary key of the same table.
---
### Types of joins
1. Cross join
	- Cartesian product
2. Inner join
	- Equal join : PK  = FK
3. Outer join
	- left  outer join
	- right outer join
	- full outer join
4. Self join