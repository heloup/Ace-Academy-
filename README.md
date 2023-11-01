# Team 12 MIST 4610 Group Project 1 
# Team Name 
Team 12 
# Team Members
1. Thomas Rogers @thomas3rogers
2. Morgan Emmons @morganemmons
3. Pierce Helou @heloup
# Problem Description
The problem we were tasked with was building a relational database for Ace Academy tennis club that classifies and connects their activities, members, and services offered. The main entity of the model was the Members as they represent the most important factor of the club. The members can reserve and play on the courts, participate in tournaments, buy items from the proshop, and schedule lessons with coaches. The main problem we were tasked with was building a database that could help with streamlining operations, improve member experiences, and enhance marketing efforts. Our main goal in this is to accurately fill the databases and model the relationships in order to give the management team an accurate glimpse into the data and relationships that exist wtihin their club to help spur on further improvements. (add Queries explanation)
# Data Model
Our data model for Ace Academy Tennis Club represents a comprehensive system for managing a sports club, specializing in tennis. It comprises of several interconnected entities to efficienctly handle memberships, coaching, court reservations, tournaments, and pro shop transactions. 

Since each member is important to us we wanted to track each members unique id, their name, contact information, membership type and the start and end dates of their memebership. 

Every court has a unique id, court number, and different availability times so that everyone can see when each court can be played at different times of the day. Courts can be booked by multiple members. To show this relationing we created a Reservation table to show that members can book multiple courts and courts can be booked my multiple members.

At Ace Academy we pride ourselves in our superior coaching. To keep track of each Coach each one has a unique id, name, and contact inforamtion. A coach can conduct multiple lessons and each lesson is conduced by one coach. We offer many lesson types for many dates and times. Each lesson will also contain its own unique id. To keep track of the members attedndding each lesson we decided to make a Lesson Attendence table. This tables aim was to show that members can attend multiple lessons and each lessons can have multiple attendees.

Every so oftern Ace Academy hosts tournaments. In our tournament entity we account for each tournaments ID, time, date, type, and fee. With every torunament we have a lot of particiapnts. A tournament can have multiple participants, but each particpant belongs to one tournament. When we asked our client about members playing in tournaments they said that members can participate in multiple tournaments and that tournaments can have multiple member participants. To show this relationship we created an entity called Member Tournament Participantion.

One of our main revenue drivers is our Pro Shop. With so many items and people coming through we wanted our clients to be able to have a database for every transaction. Each pro shop item has a unique id, name, price and quanitity in stock. While each transaction has a unique id, date and date. A member can make multiple transactions in the pro shop. While each transaction is made by one member. A pro shop item can be a part of multiple transactions, however each transaction includes one pro shop item. A item can exist independnetly of any transaction.
# Data Dictionary
<img width="666" alt="Screenshot 2023-10-31 at 8 02 14 PM" src="https://github.com/heloup/Ace-Academy-/assets/148908686/b3e2d6b1-4d23-4ded-a245-7f3d7cf8efa1">

<img width="627" alt="Screenshot 2023-10-31 at 8 08 19 PM" src="https://github.com/heloup/Ace-Academy-/assets/148908686/ccc84c36-5644-4142-aec0-e1cdc1784d35">


# Quereies
# Database Information
