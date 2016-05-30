# Programmeerproject

###APP PROPOSAL – ‘DE BIERLIJST’
When students live in houses with shared facilities, there often is time for drinks in the living room. Therefore it is highly preferred to have some drinks in stock, so that you can take a drink every time you want it. Then the first problem will arise, namely the fact that one will drink more than another and the one who drinks less will not pay for the drinks of the one who drinks more. A solution came fast: one will tally the drinks he takes from the stock. When the stock is empty, there must be calculated who drinks for how many euros. That solution can be really useful, but the hand-written tallies can get lost and people can make the tallies really unreadable. So there is the solution: making an app for this student-problem! It is also possible to tally drinks for another person, so when one is lazy and forget to tally his/her drinks, you can do it yourself. The only rule is to keep it fair! Although the name of the app is ‘Beer List’, all drinks are possible to add.
### Features
The app will have different features, the most basic  and required features are the following:
-	Able to make groups and invite people by mail
-	Keeps track of who buys what drinks at what price
-	Keeps track of who drinks what by tally every drink you take
-	Keeps track of the balance of every user 
-	Keeps track of the stock<br><br>
When the time allows it, there will also be additional features:
-	Implement push-messages when the stock of a certain drink is empty
-	Implement push-messages when your balance is low or when you have the lowest balance so you have to buy new drinks
-	Implement chat-functions or other social things 
-	Implement a function whereby you can click on the group, see all the users and get more information about a user when clicking on the user. Information like his/her balance, login name etc.
-	Users can participate in multiple groups.<br>

### Dataset
The app is based on an online database, because all up-to-date data must be seen by everyone at every moment. This will be done by a MySQL-Database, that will be based on phpMyAdmin. With this, all the information of the users will be stored. Probably the database will be stored at a webserver of my own. The following things must be stored in the database: login name, password, mailadress, what drinks a user have bought, what price the drinks were, how much and what kind of drinks the user has drink. There are mutual relations between the stored things because the price is related to the kind of drink for example. 
Important for this app is that the interface of Android works together with the online SQL-database. So, first of all it is necessary to connect the interface and the database well, because otherwise nothing in the app will work. The whole app is based on the database, because it is all about keeping track of information. 
Within the app, my own API-request has to be used. That request will ask for the information from the database. So, the API-request will be the http-link towards the database. No further external APIs are needed.

### Difficulties
Problems that can occur are difficulties with combining Android studio with the database. That can be very complex, but since there are a lot of tutorials and explanations about how to combine these two, the struggle will hopefully be limited. Another problem can be the fact that every user must see something else. A user should only see his own balance at the bottom and not just from every group member. That kind of things can give some problems. Another thing that seems to be somewhat difficult is the tally-thing. When you click on a person, you have to select the drink and then a tally must be seen in the app. That tally stands for the count of one drink, and the database has to know that too. Also the fact that with 5 tallies, it shouldn’t be five stripes behind each other, but four stripes with one stripe through the other four. I think there will occur a lot of ‘little’ problems, like it seems to be easy to solve but it is somewhat more complicated.
### Inspiration 
This app is partly based on the website www.bierlijst.nl, whereby the idea of this app is the same but it is only a digital version. The differences are that the bierlijst.nl only allows beers, and this app allows every drink because the user can add a name him/herself and therefore all drinks are possible. They have also used a MySQL-database for this, but because it is only a web-version, they don’t have to work with Android studio and combining it.


