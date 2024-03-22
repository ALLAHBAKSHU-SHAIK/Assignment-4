# Assignment - 4
Creating a Database Using MongoDB and Mongosh

1. Database Setup
- Open the mongoDB compass 
- Create a new MongoDB database: myDatabase  
 
2.	Collection Creation:  
- Create a collection within database: users  
![alt text](image.png)

3.	Document Insertion: 
-	Insert five documents into the users collection, each representing a user with fields such as name, email, and age. 
-	Before inserting into collection “use db” command to switch the current database context within MongoDB. 
-	db.users.insertMany() method is used to insert the documents into users collection as shown below. 
![alt text](image-2.png)
4.	Queries to retrieve:  
-	To retrieve all the users from the users collection.  o db.users.find({ }); 
![alt text](image-1.png)
-	To retrieve the specific users with an age greater than or equal to 
30 o db.users.find({ Age: { $gte: 30 } });  
![alt text](image-3.png)
5.	Update Operation:  
-	To update the age of a user with a specific email address in MongoDB, use the updateOne() method.  
-	Example: 
o Db.users.updateOne( 
	   	 	{ Name: "Bakshu" }, 
	   	 	{ $set: { Age: 24 } } 
	 	); 
![alt text](image-4.png)
6.	Deletion Operation:  
-	To delete the user document based on a specific email address in MongoDB, you can use the deleteOne() method. 
db.users.deleteOne({Email: asif@gmail.com});
![alt text](image-7.png)
7.	Index Creation: 
- To create an index on the email field of the users collection in MongoDB, use the db.users.createIndex() method. 
    - db.users.createIndex({ Email: 1 }); 
![alt text](image-6.png)
## Final Outcome: 
![alt text](image-5.png)