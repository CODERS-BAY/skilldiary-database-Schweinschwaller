# SKILL DIARY GEORG SCHWEINSCHWALLER

## Monday 24.08.2020

+ all the organizational stuff
    - eAMS
    - devices and books
    - rules
  
    1. punctuality
    2. cleanliness / hygiene / neatness
    3. friendly treatment
    4. helpfulness
    5. understanding
    6. break together / fresh air
    
+ resume
    - writen in markdown
    - uploaded with Gitkraken
+ GitKraken
    - mylife
    - skilldiary  
+ Markdown
    - see readme.md
    - https://markdown-it.github.io/

---
## Wednesday 26.08.2020

DB have to fulfill 9 rules

+ Integration
    - datamanagment is not redundant
+ Operation
    - save, search, change, paste
+ Cataklog
    - datainfos means metadaten
+ Recognition views
    - rights (admin, user, poweruser)
+ Integrity assurance
    - the data don't get corrupted
+ Access control
    - yeah rights again
+ Transactions
    - put some operations together. so they get alle down or none of them
+ Synchronization
    - more then one person can work with the databank
+ Datensicherung
    - backup

Data modeling

To get scheme use this 4 kinds

Relationship is a rout
Entity is a box
attribut is eclise
and by the key attribut is the text underlined

there are 4 Cardinality 
1:1, 1:N, N:1, M:N

example: rental car 

a rental car have more then one driver and a driver can have more then one car => the Entiy driver have a Relationship rent for the entiy car with a Cardinality of M:N

DB have a loot of datatyps google it if u need to<br>
importan is that string in DB is varchar!
timestamp is a date<br>
(int,double,...)

If you have 3 entiy that stays in relationship do the cardinality in that order Left->Button Left->Rigth Rigth->button

A entiy can have a relationship to it self. <br>
example a student is responsible for it self.

Relationships can also have attibutes

---
## Wednesday 2.09.2020

Assiatative tabel

When you have a M:N relationship you need a Assiattive tabel. 

Example: Teacher --M- teach -N-- Class

Teacher -1--N- teach_Teacher_Class -N--1- Class

In the now entity are the keys of the to others entities.<br>
Teacher(<ins>teacher_SVN</ins>, name, .....)<br>
Clas(<ins>class_ID</ins>, name, .....)<br>
teach_Teacher_Class(<ins>teacher_SVN</ins>,<ins>class_ID</ins>)<br>

The key attribute is always <ins>underlined</ins>.<br>

Consistency of data is: When you change an attribute like name, all attribute that contains that data changed. So ther is no corruption.

There are three anomalies that can create corruption.<br>
+ <ins>update</ins><br>
it may not be changed more or less than requested<br>
+ <ins>insent</ins><br>
no more or less than requested may be inserted<br>
+ <ins>delete</ins><br>
no more or less than requested may be deleted<br>

Redundancy in a DB is bad. If a name is saved 2 times and one will be changed. You do't know witch name is now true, because you have 2 differed entry.

<br>
<ins><strong>Normal Form</strong></ins>

For the first normal form you have to bring the elements to an atomar state.<br>
Example:<br>
address: Lilienstraße 8, 4400 Steyr

to

street: Lilienstraße<br>
buildingnumber: 8<br>
plz: 4400<br>
city: Steyr<br>

The Problem with the first normal form is that, there can be redundancy. So you need the secound normal form.

By the secound normal form the attibutes respectively to the keyattibute.
Eine Relation ist in 2NF, wenn sie in 1NF ist und jedes nicht dem Schlüssel angehörende Attribut voll funktional abhängig ist vom Gesamtschlüssel.

In the third normal form the attibutes that not keys are independently to each other.

---
## Wednesday 9.09.2020

At a 1 to N relationship you can have to put the primekey form the (1)side in the (N)side as Foreign key 

if you Assiatative tabel a tabel you can use the 2 Foreign key as prime key 

---
## Wednesday 16.09.2020

Object oriented DBMs​ - No SQL​
The goal of object-oriented databases is to be able to store the objects of the programming language, without reshaping or disassembling them.​
Object databases are used to store objects directly, without having to worry too much about normalization of ID referencing.​
The database itself takes care of the assignment of unique IDs to the stored objects and the assignment of objects to one another.​
This means that the individual linked objects can still be addressed directly via methods even after they have been saved.​
Object databases shows thier strengths with very complex problems.​
If you have many simple queries, they are slower compared to typical relational systems.​

No SQL​ (Not only SQL) ​
NoSQL brefers to databases that follow a non-relational approach​
NoSQL-systems work with versioning of data and conversions in the context of background processes​
BASE ​(Basically Available, Soft State, Eventually Consistent) ​
Instead of ACID ​(Atomicity, Consistency, Isolation, Durability)   ​
With BASE, the focus is on the availability and less on the consistency of the data.​
The data may just be consistent or, to put it optimistically, almost always consistent. ​

Key/Value - database systems
A key-value store is a database which uses an array of keys where each key is associated with only one value in a collection. ​
It is quite similar to a dictionary or a map data structure. Key-value stores can be considered as the most primary and the simplest version of all the databases​

Key/Value - database systems​
Key/Value-Systems has a key and value scheme​.
These keys can be divided into namespaces and databases.​
The values of the system can also contain lists, sets or hashes.​

Column-oriented database systems​
This arrangement of the columns has advantages. ​
During the reading process of data, no unnecessary information is read, instead only the information that has been selected to speed up read access.​
The writing process is just as quick when it comes to a single column.​

Document-oriented databases​
A document database is a type of nonrelational database that is designed to store and query data as JSON-like documents.​
The data in a document is stored in the form of key / value pairs, so it consists of a number of named key fields, each of which is assigned a specific value. ​
Arrays are also possible as values, not just atomic values.​

Graph model and systems​
Graphs are used to represent a diversity of problems through nodes, edges and their relationships.​
Examples: ​
Navigation system, saves the road maps in the form of a graph.​
The structure of the internet with links to the pages can be mapped with a graph model.​