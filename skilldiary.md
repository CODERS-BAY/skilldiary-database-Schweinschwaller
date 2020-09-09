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

In the third normal form the attibutes that not keys are independently to each other.

---
## Wednesday 9.09.2020

At a 1 to N relationship you can have to put the primekey form the (1)side in the (N)side as Foreign key 

if you Assiatative tabel a tabel you can use the 2 Foreign key as prime key 