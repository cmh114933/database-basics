### How do websites store information for display?

+++

### Boss requirements

- Show laptop sales for 2019
- where address is somewhere in Beach Street
- and sales is greater than 3000
- model is inspiron or latitude
- ordered by date and grouped by product

+++

### Additional Requirements

- Grouped together by country
- Grouped together by state
    - where state population is more than 500k
- where laptop cumulative sales is greater than 100k units

+++

What sort of information do the following websites store for display?
- School
- Facebook

+++

### Ways to store

+++

- Text file

```
id, name, age
1, John Smith, 18
2, Jane Doe, 20
3, Donald, 16
```

+++

- Tables (Excel/ Google Sheet)

|id|name|age|
|---|---|---|
|1|John Smith| 18|
|2|Jane Doe| 20|
|3|Donal| 16|

---

### Laptop Sales
[Link here](https://docs.google.com/spreadsheets/d/1aoycRdgvbkgsxfIKDVdU8w1ZaSwz4zs8MAzh8UYR4HI/edit#gid=0)

+++

One big table
- Redundant 
- Conflicting
- Difficult to update

+++

### Organized Laptop Sales
[Link here](https://docs.google.com/spreadsheets/d/1H7Q4gxrL4lqf_nU2DjzA6xJkz4biUEer8dK0Imm1XfQ/edit#gid=1408105866)


+++

Separated Tables
- Easy to update (Single source)
- Not redundant or conflicting

---

### What is a database?
- Database is an **organized collection** of data
- i.e: Data stored in a specific structure, commonly in the form of `Columns/Field` and `Rows/Records`
- Database become more organized and versatile when you include relationships

+++

### Database vs Spreadsheets
- Spreadsheets can only store as much data as the number of rows and columns
- Accessing/filtering values in spreadsheets are tedious and not as fast and efficient
- SQL is specifically designed to handle querying databases
- Updating and managing spreadsheets is error prone. 
- Spreadsheet data is prone to redundancy and conflicts.

+++

Separated tables are connected via **primary key** and **foreign key** pairs, which denote the relationship

+++

- Primary Key is
    - a unique identifier for a record in a table
    - cannot be null
    - only one in table
- Foreign Key is
    - a primary key on another table (serves as the reference that denotes relationships between entities)
    - can be null
    - can have multiple in a table

---

### What is an Entity Relationship Diagram?
- A visual representation of a database's schema and relationship, denoted by entities (or, tables).

+++

### Address Book ERD
- https://dbdiagram.io/d

```
table contacts {
  id integer [pk]
  name string
  contact_no string
  birthday date
  contact_list_id integer
}

table users {
  id integer [pk]
  username string
  password varchar
}

table contact_list {
  id integer [pk]
  user_id integer
}

Ref: "users"."id" < "contact_list"."user_id"

Ref: "contact_list"."id" < "contacts"."contact_list_id"
```

---

### Hands On!
To Do List Application

+++
A todo list can:
1. show the actual text for the todo
2. show whether the todo is completed
3. show when the to do was added
4. show an id to uniquely identify the todo
5. show date of completion for todo

+++

A todo list app has multiples users, where each user:
1. has a first name
2. has a last name
3. has an email address

+++

A user can create many todo lists, and each list is composed of many todo items.
- Denote this relationship using primary key and foreign keys.

---

Exercise

+++

### Identify the relationships

<img src="https://s3-ap-southeast-1.amazonaws.com/next-neo-images/images/f1b8324f-0604-4ea5-87c3-dbd3cf8e1a3e-sql_assignment.png" />

Hint* : There are 14 relationships in total

+++

### Replicate the schema in dbdiagram

+++

### Group assignment

Split into groups of 3-4 and create the schema for one of the following topics:

1. School
  - Classroom
  - Teachers
  - Departments
  - Students
  - Topic
  - Grades

+++

2. Hospital
  - Doctors
  - Nurses
  - Patients
  - Wards
  - Bed

+++

3. Lazada 
  - Categories
  - Products
  - Sellers
  - Buyers
  - Orders
  - LineItems

+++

4. AirBnB
  - Owners
  - Tenants
  - Properties
  - Tags
  - Booking