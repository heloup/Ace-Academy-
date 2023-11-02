# Team 12 MIST 4610 Group Project 1 
# Team Name 
15061 Team 12 
# Team Members
1. Thomas Rogers [@thomas3rogers](https://github.com/thomas3rogers)
2. Morgan Emmons [@morganemmons](https://github.com/morganemmons)
3. Pierce Helou [@heloup](https://github.com/heloup)
# Problem Description
The problem we were tasked with was building a relational database for Ace Academy tennis club that classifies and connects their activities, members, and services offered. The main entity of the model was the Members as they represent the most important factor of the club. We believe the members are the main entity of the model as they can interact with almost all other aspects of the model they reserve and play on the courts, participate in tournaments, buy items from the proshop, and schedule lessons with coaches. The main problem we were tasked with was building a database that could help with streamlining operations, improve member experiences, and enhance marketing efforts. Our main goal in this is to accurately fill the databases and model the relationships in order to give the management team an accurate glimpse into the data and relationships that exist wtihin their club to help spur on further improvements. (add Queries explanation)
# Data Model
Our data model for Ace Academy Tennis Club represents a comprehensive system for managing a sports club specializing in tennis. It comprises several interconnected entities to efficiently handle memberships, coaching, court reservations, tournaments, and pro shop transactions. 

Since each member is vital to us, we wanted to track each member's unique ID, name, contact information, date of birth, membership type, and the renewal date of their membership.

Every court has a unique ID, court number, and different availability times so that everyone can see when each court can be played at other times. Courts can be booked by multiple members. To show this relation, we created a Reservation table to show that members can book numerous courts, and courts can be booked by various members. Each reservation is made by one member and is specific to one court.

At Ace Academy, we pride ourselves in our superior coaching. To keep track of each Coach, each has a unique ID, name, qualifications, and area of focus. A coach can conduct multiple lessons, each run by one coach. We offer many lesson types for many dates and times. Each lesson will also contain its own unique ID. To keep track of the members attending each lesson, we decided to make a Lesson attendance table. This table shows that members can participate in multiple lessons, and each lesson can have multiple attendees.

Every so often, Ace Academy hosts tournaments. In our tournament entity, we account for each tournament's ID, time, date, type, and fee. With every tournament, we have a lot of participants. A tournament can have multiple participants, but each participant belongs to one tournament. We also wanted to keep track of all our tournament participants and their results. When we asked our client about members playing in tournaments, they said that members can participate in multiple tournaments and that tournaments can have multiple member participants. To show this relationship, we created an entity called Member Tournament Participantion.

One of our main revenue drivers is our Pro Shop. With so many items and people coming through, we wanted our clients to be able to have a database for every transaction. Each pro shop item has a unique ID, name, price, and quantity in stock. Each transaction has a unique ID, date, and date. A member can make multiple transactions in the pro shop. While each transaction is made by one member. A pro shop item can be a part of various transactions. However, each transaction includes one pro shop item. An item can exist independently of any transaction.

![Project Model Part 2](https://github.com/heloup/Ace-Academy-/assets/148258150/0ae2f7cc-27c0-4df7-bd43-235840450d91)

# Data Dictionary
<img width="587" alt="members table" src="https://github.com/heloup/Ace-Academy-/assets/148908686/4112a96d-5784-4745-8575-5813721ce85a">

<img width="557" alt="coaches table " src="https://github.com/heloup/Ace-Academy-/assets/148908686/a847feda-4e1b-49bc-951e-1f39a4cfab4b">

<img width="600" alt="Court table" src="https://github.com/heloup/Ace-Academy-/assets/148908686/8770bfbc-bf26-4350-a4c0-6e028b2772e1">

<img width="602" alt="reservation table" src="https://github.com/heloup/Ace-Academy-/assets/148908686/baa53d09-cf54-4817-9d54-ac0fbf84144f">

<img width="634" alt="tournament table" src="https://github.com/heloup/Ace-Academy-/assets/148908686/3d36ed56-1c37-44ad-8502-fe22377f443b">

<img width="607" alt="court for tournament table " src="https://github.com/heloup/Ace-Academy-/assets/148908686/ec50837b-7539-4654-87ba-aff20c4e36b5">

<img width="605" alt="tournament participants table" src="https://github.com/heloup/Ace-Academy-/assets/148908686/87af4626-f26b-4875-b5d7-6d325c659178">

<img width="633" alt="items table" src="https://github.com/heloup/Ace-Academy-/assets/148908686/560c169e-cea5-40af-add7-2d361d1f4346">

<img width="631" alt="pro shop table" src="https://github.com/heloup/Ace-Academy-/assets/148908686/8ca0cfc9-993c-4246-a25a-b9a7c64103a8">

<img width="632" alt="lessons table" src="https://github.com/heloup/Ace-Academy-/assets/148908686/a1f3336e-d19d-4511-b829-89035c246e45">

<img width="635" alt="lesson attendance table" src="https://github.com/heloup/Ace-Academy-/assets/148908686/97d347c3-445c-4d1b-a28a-4a29d82d9900">

<img width="664" alt="Member tournament participation table " src="https://github.com/heloup/Ace-Academy-/assets/148908686/e1b3deeb-f8a9-49be-8c42-a87eabdc2653">

# Quereies
**Query 1**: Query 1 shows the amount of court reservation fees owed by each member who has reserved courts. It lists the Members Id, Their first and last name and the amount of fees owed and is ordered in order of amount owed.
Code:

![Query 4610 Project 2](https://github.com/heloup/Ace-Academy-/assets/148258161/19724722-b80e-4f74-8654-1242a74cd317)


This query allows the management team to see how much outstanding fees they are owed by each member. This code allows the management to see how much fees need to be charged to each customer account. The query is labeled in order of greatest fee owed in order to ensure the most expensive fees are billed first to have less accounts recievable outstanding hopefully. 

**Query 2**: Query 2 shows the names of the members who are trained by Level 4 certfied coaches it does this by using multiple joins and multi condition wheres.

![Query 1 4610](https://github.com/heloup/Ace-Academy-/assets/148258161/25db50e7-798f-4a81-9d4a-0742d68632e8)

This query allows the heads of the club to see which of their members are being trained by the highest level of coaching. This gives the Managers a better idea of who the best players in their club are. This query also ensures that the members do not just list the coach as their coach but also is actively taking lessons from the coach. This query gives the managers a better idea of the skill level of their club.

**Query 3**:  This Query retrieves the first names and last names of members who have a court reservation on the 1st of November, along with the corresponding court ID.

![image](https://github.com/heloup/Ace-Academy-/assets/148258150/6527eaa1-0f42-464c-87d7-6881982b6dd1)

**Query 4**:This Query shows how much Michael Williams spent at the Pro Shop, what items he bought, and the price of each item.

<img width="841" alt="Query 4" src="https://github.com/heloup/Ace-Academy-/assets/148908686/0e111bc0-c992-4cd0-86fc-d19d0dae0a73">

**Query 5**
This Query shows the quantity remaining in each item after recent pro shop purchases.
![Query 5](https://github.com/heloup/Ace-Academy-/assets/148258161/574cdadc-e001-42b2-ba5c-64a11b7b4640)

**Query 6**
This Query shows each coach and how many members each coach teaches.
![Query 6](https://github.com/heloup/Ace-Academy-/assets/148258161/cfcd451f-18d1-4114-8435-ffb136f5a542)

**Query 7**
This Query shows the most expensive items in the Pro Shop as it uses a correlated subquery to calculate the average.
![Query 7](https://github.com/heloup/Ace-Academy-/assets/148258161/adffd76d-df24-494e-ad09-317777fb0605)

**Query 8**
This Query shows how many courts each tournament used and how much money was owed for using these courts.
![Query8](https://github.com/heloup/Ace-Academy-/assets/148258161/05a11866-240c-4c6a-a4c4-a137d2ad8a39)

**Query 9**
This Query shows the names of coaches who also are members of the club by using multiple table joins and multi where clauses.
![Query9](https://github.com/heloup/Ace-Academy-/assets/148258161/97da2100-b836-4439-920a-054f9799f1bd)

**Query 10**
This Query shows which coaches teach members with premium memberships
![Query 10](https://github.com/heloup/Ace-Academy-/assets/148258161/b8d02cfd-5294-4e58-b818-db6b98b59096)

# Database Information
Name of the database: cs_g12p1

Additional Information: Each query we have listed is bookmarked through the use of stored procedures according to this format: TP_Q1();
