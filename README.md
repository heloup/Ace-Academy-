# Team 12 MIST 4610 Group Project 1 
# Team Name 
Team 12 
# Team Members
1. Thomas Rogers [@thomas3rogers](https://github.com/thomas3rogers)
2. Morgan Emmons [@morganemmons](https://github.com/morganemmons)
3. Pierce Helou [@heloup](https://github.com/heloup)
# Problem Description
The problem we were tasked with was building a relational database for Ace Academy tennis club that classifies and connects their activities, members, and services offered. The main entity of the model was the Members as they represent the most important factor of the club. We believe the members are the main entity of the model as they can interact with almost all other aspects of the model they reserve and play on the courts, participate in tournaments, buy items from the proshop, and schedule lessons with coaches. The main problem we were tasked with was building a database that could help with streamlining operations, improve member experiences, and enhance marketing efforts. Our main goal in this is to accurately fill the databases and model the relationships in order to give the management team an accurate glimpse into the data and relationships that exist wtihin their club to help spur on further improvements. (add Queries explanation)
# Data Model
Our data model for Ace Academy Tennis Club represents a comprehensive system for managing a sports club specializing in tennis. It comprises several interconnected entities to efficiently handle memberships, coaching, court reservations, tournaments, and pro shop transactions. 

Since each member is vital to us, we wanted to track each member's unique ID, name, contact information, date of birth, membership type, and the renewal date of their membership.

Every court has a unique ID, court number, and different availability times so that everyone can see when each court can be played at other times. Courts can be booked by multiple members. To show this relation, we created a Reservation table to show that members can book numerous courts, and courts can be booked by various members.

At Ace Academy, we pride ourselves in our superior coaching. To keep track of each Coach, each has a unique ID, name, qualifications, and area of focus. A coach can conduct multiple lessons, each run by one coach. We offer many lesson types for many dates and times. Each lesson will also contain its own unique ID. To keep track of the members attending each lesson, we decided to make a Lesson attendance table. This table shows that members can participate in multiple lessons, and each lesson can have multiple attendees.

Every so often, Ace Academy hosts tournaments. In our tournament entity, we account for each tournament's ID, time, date, type, and fee. With every tournament, we have a lot of participants. A tournament can have multiple participants, but each participant belongs to one tournament. We also wanted to keep track of all our tournament participants and their results. When we asked our client about members playing in tournaments, they said that members can participate in multiple tournaments and that tournaments can have multiple member participants. To show this relationship, we created an entity called Member Tournament Participantion.

One of our main revenue drivers is our Pro Shop. With so many items and people coming through, we wanted our clients to be able to have a database for every transaction. Each pro shop item has a unique ID, name, price, and quantity in stock. Each transaction has a unique ID, date, and date. A member can make multiple transactions in the pro shop. While each transaction is made by one member. A pro shop item can be a part of various transactions. However, each transaction includes one pro shop item. An item can exist independently of any transaction.
![Project 1 Data Model](https://github.com/heloup/Ace-Academy-/assets/148258150/07573c48-7abd-46ff-8e8b-8653748532bd)

# Data Dictionary
<img width="666" alt="Screenshot 2023-10-31 at 8 02 14 PM" src="https://github.com/heloup/Ace-Academy-/assets/148908686/b3e2d6b1-4d23-4ded-a245-7f3d7cf8efa1">

<img width="627" alt="Screenshot 2023-10-31 at 8 08 19 PM" src="https://github.com/heloup/Ace-Academy-/assets/148908686/ccc84c36-5644-4142-aec0-e1cdc1784d35">


# Quereies
Query 1: Query 1 shows the amount of court reservation fees owed by each member who has reserved courts. It lists the Members Id, Their first and last name and the amount of fees owed and is ordered in order of amount owed.
Code:
Execute:
> select idMembers, f_name, l_name, sum(fee) from Members 
join Reservation on Members.idMembers= Reservation.Members_idMembers
join Court on Reservation.Court_idCourt= Court.idCourt 
Group by idMembers
order by sum(fee) desc

+ -------------- + ----------- + ----------- + ------------- +
| idMembers      | f_name      | l_name      | sum(fee)      |
+ -------------- + ----------- + ----------- + ------------- +
| 5              | James       | Davis       | 40            |
| 3              | Michael     | Williams    | 30            |
| 1              | John        | Smith       | 25            |
| 2              | Sarah       | Johnson     | 20            |
| 4              | Laura       | Brown       | 15            |
+ -------------- + ----------- + ----------- + ------------- +
5 rows

This query allows the management team to see how much outstanding fees they are owed by each member. This code allows the management to see how much fees need to be charged to each customer account. The query is labeled in order of greatest fee owed in order to ensure the most expensive fees are billed first to have less accounts recievable outstanding hopefully. 

  
# Database Information
