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

source
https://payberah.github.io/files/download/dic/NoSQL%20Databases.pdf


---
## Wednesday 23.09.2020

# DB-Test
## Aufgabe 1
Stelle Entitäten mittels Chen-Notation und Min,Max Notation dar.
Wähle ein sinnvolles Beispiel!
<pre>
___________                          ___________
| Kamera   |_1,1____schießt____1,*__ |   Foto  |
|__________|                         |_________|
</pre>

## Aufgabe 2
Kann eine Beziehung Attribute haben?
Wenn ja, wie stelle ich es im ERD dar?
<pre>
___________                          _____________
| Lehrer  |_1___ teach subject ___N__|  Schüler  |
|_________|           |              |___________|
                    Mark
</pre>
## Aufgabe 3
Welche Codd'schen Anforderungen gibt es (Nenne mindestens 5)

Katalog
Operation
Benutzerschichten
Integration
Transaktion
Integretätssicherung
Datensicherung
Zugriffskontrolle

## Aufgabe 4
Nenne den Unterschied zwischen Konzeptuellen und Logischem Schema

Konzeptuellen Schema ist eine wolke in dem die Entity und Attribute.
in einem Logischen Schema sind die Entity mit relationships verbunden und Attribute sind den Entitys und relationships zugewiesen.

## Aufgabe 5
Welche 3 Bestandteile gibt es im Entity Relationship Model

Entity 
Releationship 
Attribut

## Aufgabe 6
Welche Datentypen gibt es in MySQL? (Nenne mindestens 5)

varchar
int
boolean
double
float
char
timestamp

## Aufgabe 7
Welche Arten von Schlüsseln gibt es und welche Eigenschaften besitzen diese?#

PrimärSchlüssel: Identifizieren die Tabele es kann eine generierte ID sein oder ein natürlicher Schlüssel der einzigartig ist wie die SVN einer Person

FremdSchlüssel: verweist auf eine anderen Datensatz

## Aufgabe 8
Welche Arten von Beziehungen gibt es? Zeichne für jede ein Beispiel auf
<pre>
unäre
____________
| Schüler  |
|__________|
|          |
|Erziehungs|
 berechtigt

duale(binär)
____________                        ___________
| Kamera   |_1____ schießt _____N__ |   Foto  |
|__________|                        |_________|
                   
Trinäre
____________                          ____________
| Entity A |__M____ relatioship ___N__| Entity B |
|__________|  M          |         M  |__________|
                       N | N
                   |¯¯¯¯¯¯¯¯¯¯¯|
                   | Entity C  |
                   ¯¯¯¯¯¯¯¯¯¯¯¯¯
</pre>
## Aufgabe 9
Was bedeutet der Begriff Kardinalität und welche Kardinalitäten gibt es?

Sie geben an wie die Beziehung der Entitys sind

1:1             Ein Ehepartner hat genau einen Ehepartner
1:N (N:1)       Eine Kamera schießt viele Fotos, aber ein Foto wurde genau nur von einer Kamera geschoßen
M:N             Ein Kunde kauft viele Artikel und ein Artikel wird von vielen Kunden gekauft

## Aufgabe 10
Was bedeutet der Begriff Datenintegrität und worin unterscheidet sich Integrität und referentielle Integrität?

Datenintegrität beschreibt die Korrektheit der Daten.
Referentielle Integrität beschreibt die Korrektheit der Beziehungen.

## Aufgabe 11
Erkläre die 3 Normalformen

In der ersten Normalform werden die Datensätze auf Atomare Form heruntergebrochen
In der zweiten Normalform sind alle Daten vom PrimärSchlüssel abhänig.
In der dritten Normalform sind die Daten die keine Schlüssel sind unabhänig von einander.

## Aufgabe 12
Erkläre den Unterschied zwischen starken und Schwachen Entitäten und erstelle ein Beispiel.

Schwache Entitäten sind nur in Kombination mit dem Schlüssel der starken Entity identifizierbar.

## Aufgabe 13
Welche Grundregeln gibt es im Relationenmodell? (Nenne mindestens 4)

Bei der Textuelle notation in den die Entity mit den Attribute und den Datentypen
PrimärSchlüssel sind unterstriechen.
FremdSchlüssel sind strichliert unterstriechen.

## Aufgabe 14
Wie löst man eine M:N Beziehung auf? Erstelle ein Beispiel
<pre>
______________                    _____________
| Hersteller |_M___produziert___N_|  Artikel  |
|____________|                    |___________|
______________        ______________       _____________ 
| Hersteller |_1___N_ | produziert |_N___1_|  Artikel  |
|____________|        |_A_H________|       |___________|

produziert_A_H ist eine Entity
in produziert_A_H stehen die Schlüssel von Hersteller und Artikel als Fremdschlüssel (diese beiden Fremschlüssel werden als PrimärSchlüssel hergenommen)
</pre>

## Aufgabe 15
Ein Handelsbetrieb verkauft ein Sortiment von Artikeln, die er von verschiedenen Herstellern bezieht. Der Handelsbetrieb hat einen bestimmten Kundenkreis, der regelmäßig Bestellungen aufgibt. Eine Bestellung kann mehrere Artikel umfassen. Ein Artikel kann von mehreren Lieferanten bezogen werden und ein Lieferant liefert natürlich meist mehr als einen Artikel. Erstelle ein ERD und ein Relationenmodell, welches der 3. Normalform entspricht.
<pre>
______________        ______________       _____________        ___________       _____________
| Hersteller |_1___N_ | produziert |_N___1_|  Artikel  |_1___N_ | bezieht |_N___1_| Lieferant |
|____________|        |_A_H________|       |___________|        |_A_L_____|       |___________|
                                                |       _______________       ______________
                                                ∟_1___N_| umfasst_A_B |_N___1_| Bestellung |
                                                        |_____________|       |____________|

Hersteller:
Key:    Hersteller_ID: int
        Name: varchar
        Adresse: varchar
        ...

produziert_A_H:
key,fkey:   Hersteller_ID: int
key,fkey:   Artikel_ID: int

Artikel:
key:    Artikel_ID: int
        Name: varchar
        Beschreibung: varchar
        ...

bezieht_A_L:
key,fkey:    Artikel_ID: int
key,fkey:    Lieferant_ID: int

Lieferant:
key:    Lieferant_ID: int
        name: varchar
        Beschreibung: varchar
        ...

umfasst_A_B:
key,fkey:    Artikel_ID: int
key,fkey:    Bestellung_ID: int

Bestellung
key:    Bestellung_ID: int
        name des Kunden: varchar
        Adresse: varchar
        ...
</pre>

## Aufgabe 16
Welche Anomalien kennst du und was beschreiben sie?

Erstellungs Anomalien, Änderungs Anomalien und die Lösungs Anomalien

Es sollen immer nur so viel Daten ein getragen werden wie angegeben
Es sollen immer nur genau so viele Daten geändert werden wie angegeben
Es sollen immer nur genau so viele Daten gelöscht werden wie angegeben 
sonst entsteht eine Anomalie.

## Aufgabe 17
Modellieren Sie den angeführten Realitätsausschnitt einer Fluggesellschaft mit Hilfe eines Entity Relationship- Diagramms. Treffen Sie, falls notwendig, sinnvolle Annahmen und dokumentieren Sie diese nachvollziehbar in Ihrer Lösung. Der zu betrachtende Realitätsausschnitt der Fluggesellschaft umfasst folgenden
Sachverhalt:
Flughäfen haben ein Kürzel (= Schlüssel) und gehören zu einer Stadt (z.B. „FRA“ für Frankfurt, „FCO“ für Roma Fiumicino).
Flüge haben eine Flugnummer (z.B. „LH 306“), führen von einem Flughafen zu einem anderen, mit jeweils einer festen Abflugs- und Ankunftszeit (z.B. ab Frankfurt um 07:30 nach Roma Fiumicino mit Ankunft um 09:15).
Jeder Flugzeugtyp hat einen Namen (z.B. „747-400“) und eine Sitzanzahl (z.B. 430 Sitze).
Piloten haben einen Namen (z.B. „Meier“), ein Geburtsdatum (z.B. „1.1.1960“) und eine Berechtigung, bestimmte Flugzeugtypen zu fliegen (z.B. „747-400“ und „A310“).
Jedes einzelne Flugzeug ist von einem bestimmten Flugzeugtyp (z.B. „747-400“) und hat einen Namen (z.B. „Mozart“).
Bei einem Flug-Einsatz wird ein Flug (z.B. „LH 306“) an einem bestimmten Datum (z.B. „6.2.2011“) von einem bestimmten Piloten (z.B. „Meier“) mit einem bestimmten Flugzeug (z.B. „Mozart“) geflogen.
Bilden Sie das konzeptuelle Schema in ein relationales Schema ab. Das relationale Schema soll der 3. Normalform genügen
<pre>
________                _____________       ____________        ____________       _____________
| Flug |_N__startet__1__| Flughafen |_1___N_| Flugzeug |_1___N_ | fliegt   |_N___1_| Pilot     |
|______|_N__landet___1__|___________|       |__________|        |_FZ_P_____|       |___________|
  |   |                                           |                                       |
  |   ∟__1________einsatz______________________1__|                                       |
  |                                                                                       |
   ∟__1___________dienst_______________________________________________________________1__|

Flughafen:
key:    Kürzel: varchar
key:    StadtKürzel: varchar

Flug:
key:    Flugnummer: int
fkey:   AbflugFlughafen
            -Kürzel
            -StadtKürzel
fkey:   AnkunftFlughafen
            -Kürzel
            -StadtKürzel
        Ankunftzeit: timestamp
        Abflugzeit: timestamp
        datum: timestamp

Flugzeug:
key:        Flugzeug_ID: int
key,fkey:   Flugnummer: int
            Flugzeugtyp: varchar
            Sitzanzahl: int

fliegt_FZ_P:
key,fkey:    Flugzeug_ID: int
key,fkey:    Pilot_SVN: int

Pilot:
key:    Pilot_SVN: int
        Namen: varchar
        Geburtsdatum: timestamp
        Berechtigung: varchar
</pre>

---
## Wednesday 30.09.2020

SQL

CREATE TABLE Passenger (
	Passenger_NR bigint PRIMARY KEY,
	First_Name varchar(32),
    Sure_Name varchar(32),
	Sex boolean,
	Titel varchar(32)
    );

INSERT INTO `passenger`(`Passenger_NR`, `First_Name`, `Sure_Name`, `Sex`, `Titel`) VALUES ('10','Georg','Arbeithuber',true,'Pr.')

---
## Wednesday 07.10.2020

SELECT * FROM `aircraft` WHERE `Aircraft_Name` IS NOT NULL;
Show all aircrafts with a name
<pre>
Internationale_ID  |  Airline_ID  |  Installation_Date  |  Aircraft_Name
ADE1592AD23           1322158        2020-10-01            WarWick
PON18298QWE21         5511           2010-07-15            Yuumi
</pre>

UPDATE `aircraft` SET `Airline_ID`=1234 WHERE `Aircraft_Name`='WarWick';
change all Airline_ID by aircraft where the name is WarWick to 1234
<pre>
Internationale_ID  |  Airline_ID  |  Installation_Date  |  Aircraft_Name
ADE1592AD23           1234           2020-10-01            WarWick
PON18298QWE21         5511           2010-07-15            Yuumi
</pre>

UPDATE `aircraft` SET `Airline_ID`=1234;
change all Airline_ID to 1234
<pre>
Internationale_ID  |  Airline_ID  |  Installation_Date  |  Aircraft_Name
ADE1592AD23           1234           2020-10-01            WarWick
PON18298QWE21         1234           2010-07-15            Yuumi
</pre>

INSERT INTO `aircraft` (`Internationale_ID`, `Airline_ID`, `Installation_Date`, `Aircraft_Name`) VALUES ('9999', '1111', '2020-10-10', 'TEST');
add an aircraft
<pre>
Internationale_ID  |  Airline_ID  |  Installation_Date  |  Aircraft_Name
9999                  1111           2020-10-10            TEST
ADE1592AD23           4321           2020-10-01            WarWick
PON18298QWE21         1234           2010-07-15            Yuumi
</pre>

DELETE FROM `aircraft` WHERE `Aircraft_Name` = 'TEST' AND `Airline_ID` = 1111 OR`Internationale_ID` = 9999
remove all aircrafts that have the name TEST and is in the airline 1111 or have the internationale ID of 9999
<pre>
Internationale_ID  |  Airline_ID  |  Installation_Date  |  Aircraft_Name
ADE1592AD23           4321           2020-10-01            WarWick
PON18298QWE21         1234           2010-07-15            Yuumi
</pre>

ALTER TABLE bording_card ADD FOREIGN KEY (Passenger_NR) REFERENCES passenger(Passenger_NR)
ALTER TABLE bording_card ADD FOREIGN KEY (Flight_ID) REFERENCES flight(Flight_ID)
ALTER TABLE change the table 
ADD FOREIGN KEY adds an ForeignKey (the bracket are importent)
REFERENCES is the freference tabel for the key


CREATE TABLE distance (
	Port_1_ID varchar(8) NOT NULL,
    Port_2_ID varchar(8) NOT NULL,
    distance_km bigint,
    PRIMARY KEY (Port_1_ID, Port_2_ID),
    FOREIGN KEY (Port_1_ID) REFERENCES Airport(Port_ID),
    FOREIGN KEY (Port_2_ID) REFERENCES Airport(Port_ID)
);
Create a table were Port_1_ID and Port_2_ID are the Primary key and they are Foreign Keys


ALTER TABLE bording_card RENAME TO boarding_card
change the name of the table

SELECT * FROM `aircraft`
<pre>
Internationale_ID  |  Airline_ID  |  Installation_Date  |  Aircraft_Name
5555                  5555           2020-08-02            DBMS - BDSM
6666                  4444           2020-07-02            Help ME
7777                  3333           2020-01-02            Tree
8888                  2222           2020-10-02            Solitär
9999                  1111           2020-10-01            TEST
ADE1592AD23           4321           2020-10-01            WarWick
PON18298QWE21         1234           2010-07-15            Yuumi
</pre>


SELECT * FROM `aircraft` WHERE `Aircraft_Name`LIKE 'W%'
all Aircraft name that have a W in there name
<pre>
Internationale_ID  |  Airline_ID  |  Installation_Date  |  Aircraft_Name
ADE1592AD23           4321           2020-10-01            WarWick
</pre>

SELECT `Aircraft_Name` FROM `aircraft` WHERE `Aircraft_Name`LIKE 'T%'
all Aircraft name that have a T in there name
<pre>
Aircraft_Name
Tree
TEST
</pre>

SELECT `Aircraft_Name` FROM `aircraft` WHERE `Aircraft_Name`NOT LIKE 'T%'
All Aircraft Name that don't have a t in the name
<pre>
Aircraft_Name
DBMS - BDSM
Help ME
Solitär
WarWick
Yuumi
</pre>

SELECT * FROM `aircraft` WHERE `Installation_Date` BETWEEN '2010-10-10' AND '2030-10-10'
all aircraft that were installed between 2010-10-10 and 2030-10-10
<pre>
Internationale_ID  |  Airline_ID  |  Installation_Date  |  Aircraft_Name
5555                  5555           2020-08-02            DBMS - BDSM
6666                  4444           2020-07-02            Help ME
7777                  3333           2020-01-02            Tree
8888                  2222           2020-10-02            Solitär
9999                  1111           2020-10-01            TEST
ADE1592AD23           4321           2020-10-01            WarWick
</pre>

SELECT * FROM `aircraft` ORDER BY `Aircraft_Name` DESC
<pre>
Internationale_ID  |  Airline_ID  |  Installation_Date  |  Aircraft_Name
PON18298QWE21         1234           2010-07-15            Yuumi
ADE1592AD23           4321           2020-10-01            WarWick
7777                  3333           2020-01-02            Tree
9999                  1111           2020-10-01            TEST
8888                  2222           2020-10-02            Solitär
6666                  4444           2020-07-02            Help ME
5555                  5555           2020-08-02            DBMS - BDSM
</pre>

SELECT * FROM `aircraft` ORDER BY `Aircraft_Name`
<pre>
Internationale_ID  |  Airline_ID  |  Installation_Date  |  Aircraft_Name
5555                  5555           2020-08-02            DBMS - BDSM
6666                  4444           2020-07-02            Help ME
8888                  2222           2020-10-02            Solitär
9999                  1111           2020-10-01            TEST
7777                  3333           2020-01-02            Tree
ADE1592AD23           4321           2020-10-01            WarWick
PON18298QWE21         1234           2010-07-15            Yuumi
</pre>


Bewerbungs Theme:
https://themeforest.net/item/watson-vcard-resume-cv-portfolio-template/22526409
