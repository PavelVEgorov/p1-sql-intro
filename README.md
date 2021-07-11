## The World is ours! 🌎

In this task, you have to design and fill a database containing information about the world's countries and cities. The database should meet all modern requirements, be flexible, and not redundant. Don't forget that relational databases obey real-world logic!

### R0: Infological design

Think about which entities you will store in the database. To extract a final address from the database, you will need a few entities: _Country_, _City_, and _Street_. Think about what tables you'll need for storing these entities and what information they will contain. How will they relate to one another?

### R1: Building an ER diagram
Create an Entity Relationship Diagram to visualize which entities you will store in the database and how they will relate to each other.

### R1: DDL
Using DDL commands and your diagram from release # 1, create a database structure. Don't forget about external keys. The database's design shouldn't allow you to delete a country with existing cities, but it could allow you to change its name (or other attributes excluding the primary key). After changing the country name, its cities should remain. You should also be able to move a city to another country, no matter how strange it may sound. 🙂 
There may be some homonymous streets in different cities, but they are, in fact, _different streets!_ If a city ceases to exist, then all its streets should also disappear. The corresponding external key is responsible for this. 
### R2: Create your own planet with cities and countries 😎
Use the [INSERT](https://postgrespro.ru/docs/postgresql/13/dml-insert) (rus) command to fill your database with data. Make 5-10 countries and cities; you can have more streets, but don't get carried away since this isn't the end of the assignment!

### R3: Getting data
1. Try to output the following from the database:
2. List of countries
3. List of cities
4. List of streets
5. All countries that have cities

6. All countries without cities
7. All cities of a specific country
8. All streets in the first city
9. All streets in the largest city [Hint](#help)
10. All streets in the largest country's largest city [Tip](#help)
11. All streets in the largest city of the largest country containing the letter "E" in its name
12. And finally, all addresses in the "street, city, country" format

### R4: Whoops looks like something went wrong 🙀

Did something go wrong? Are you missing something? Are the connections broken? No problemo! In this fictional world, we can change everything with one command! Well, if not one, then, several 🙂 If you typed a mistake somewhere or just wanted to change something, you can use the [UPDATE](https://postgrespro.ru/docs/postgresql/13/dml-update) (rus) command to change any piece of data in the database. Also, don't forget about the [WHERE](https://postgrespro.ru/docs/postgresql/13/queries-table-expressions#QUERIES-WHERE) (rus) clause if you don't want to risk changing all data. It's considered good practice to update using the primary key, which you can access via a separate query. You can also nest the query into the WHERE clause of the UPDATE command.

If you think something is wrong with the database schema or decided to restructure the data, you may find the [ALTER](https://postgrespro.ru/docs/postgresql/13/ddl-alter) command helpful.

### R5: They're onto us! We need to cover our tracks!
CIA officers somehow discovered our made-up world, and they aren't loving it! All data requires urgent extermination! Clear all tables with the [TRUNCATE](https://postgrespro.ru/docs/postgresql/13/sql-truncate) (rus) command. Ensure that you erased everything by attempting to output something from the tables. If nothing appears, time to delete all tables and, finally, the database.
All done? Excellent! You did it!

That's all for now! If you ever have any questions regarding SQL commands, check the [official documentation](https://postgrespro.ru/docs/postgresql/13/index) (rus).
What are you waiting for? Time to open the documentation and proceed to the next assignment!

<a name="help"><h2>Hints</h2></a>
The largest city is the one with the most streets
The largest country is the one with the most cities
