### Design Document
Josien Jansen<br>
11162295<br>
Universiteit van Amsterdam 

### Sketches of UI
![img_4214](https://cloud.githubusercontent.com/assets/18394953/15706357/74b6f504-27f3-11e6-9fc1-8b71bf8f6d39.JPG)<br>
The first image is the global UI of the app. Every user has to create an account before he can use the app. So, the very first screen is the login activity, whereby everyone first has to register for an account. Therefore the second screen is the register screen. When the user has succesfully logged in, it's time for the MainActivity, whereby the user can see how many drinks all users have taken. When there is no group at first, a group has to be created. For the time constraint, it is only possible to be part of one group and not multiple. When the group is created and groupmembers are added, it is time to see the overview of the Beer List. There is a navigation bar at all screens, so you can easily switch between different screens. There you can add stock, see the stock, go to settings and get more information about the app. That all are separate classes,to keep it clear.<br><br><br>
![voegto](https://cloud.githubusercontent.com/assets/18394953/15706684/217c2e84-27f5-11e6-8623-76ab054938ac.png)


The second image is an addition for the MainActivity whereby you can click and long-click on the amount of a groupmember, by short-clicking on it, you can add a 'tally' by choosing the kind of drink and the amount. By long-pressing it, a specification of drunken drinks were given.<br>

### PlugIns
The most important external plugin of this app will be Firebase. Firebase is a complete platform for building mobile and web applications. Firebase provides a realtime JSON database for storing and sync your app's data and that's exactly what is needed in this app. Because Firebase works with intuitive APIs packaged into a single SDK, it is not necessary to work with any other APIs than stored in the SDK of Firebase. The whole app is based on an up-to-date database, and for now Firebase provide all the features needed for this. In the future, it would also be nice to for example combine the API of Facebook for integration with friends or other social features whereby it is easy to find your friends.

### Data sources
The data source of this app is the online database of Firebase. Firebase is based on JSON, so by parsing JSON you can get realtime information about the database in the app. 

### Database Tables
![databse opzet](https://cloud.githubusercontent.com/assets/18394953/15707811/0906a112-27fb-11e6-9a45-6c8f442bd1eb.png)<br>
This is the design of the Beer List database, that consists of two tables: user information & groupinformation. Within the user information, personal data like name, mailadres and groupnumber are stored. This table is necessary because it is useful to know what user is in what group, and naturally the personal information must also be stored. All the things about the real Beer List are stored in the table Groupinformation, like all the user_ids that are in one group, which groupnumber that is, which user_id bought drinks and drink drinks, how many the drinks costs and what the balance of the users are. 
In both tables the user_ids and group_ids are stored, so with that the two can be connected. <br>
The idea of the array-lists are as follows:<br><br>
![ids](https://cloud.githubusercontent.com/assets/18394953/15707762/d23083c4-27fa-11e6-9714-63b8b99252cf.png)

### Diagram
![diagram](https://cloud.githubusercontent.com/assets/18394953/15710320/d6c40546-2809-11e6-95e6-360b091a4428.png)<br>
####Explanation of the diagram:<br>
Before going to the Beer List itself, it is necessary to succesfully login/register with your own credentials. The right credentials must be checked in the Firebase database, hence the link with Firebase.
There will also be a Class User, with the information of the database so you can easily access it and make for example calculations for the balance part. After that, it must be checked whether the user is already joining a group or not. This is happening with CheckingGroup, and the Class Group, whereby data of the group will be stored. When there is no group found, a new group has to be created in the MakingGroup Activity.
After a group is created, the MainActivity can start. Within the MainActivity, all data should be collected from the Firebase database. 
From the MainActivity, whereby you see the homescreen (the BeerList itself), you can go to the settings,add stock etc. by the navigation menu. The Activities like settings & information don't need external stuff to function but the Add stock & Check stock also need data from the Firebase database.
