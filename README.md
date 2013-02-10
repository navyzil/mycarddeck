Application: MyCardDeck
Version: Prototype
Framework: Grails and MySQL
Developer: Denzil Gideon M. Daulo


Description:
	- A web application that lets you create, edit your decks, cards and skills

Requirements:
	- MySQL Server
	- Apache-Tomcat(7.0.14)
	
Installation:
	- Extract myCardDeckBundle.zip on any directory of your choice
		- In the apache-tomcat-7.0.14/webapps folder the myCardDeck.war is already installed
	- Extract the mycarddeck.zip to your home folder(you should see a .mycarddeck folder on your home folder, its a hidden file so you should change your views to view all hidden file)
	-Execute the following SQL Scripts in MySQL (located in MySQL folder of this bundle):
		- create_mycardgame_database.sql(Required)
		(Note: The following scripts are optional, because MyCardDeck application has a feature 
		       that will automatically creates the tables and generates its test data)
		- create_player.sql
		- create_deck.sql
		- create_card.sql
		- create_skills.sql
		- create_card_skills.sql
		- create_player_card.sql
		- create_player_deck.sql
		
Running the Application:
	- Check first the app-config.properties(located at <homefolder>/.mycarddeck/) if it matches your MySql's username and password 
	  	- Modify it if doesn't match on your MySQL credentials
 	- Check if the myCardDeck.war is located on the webapps folder of tomcat (<path>/apache-tomcat-7.0.14/webapps)
 	- Go to the bin folder(<path>/apache-tomcat-7.0.14/bin) and click startup.sh(Linux or Ubuntu - just click run on the pop up) or startup.sh(Windows) 
 	  (Note: you can also go to your terminal or command prompt and execute the sh or bat file)
 	- Open your browser(preferably Firefox) and type http://localhost:8080/myCardDeck/

Features:
	- You can choose your main deck based from your 10 chosen decks
	- It has a deck manager that will let you choose up to 10 deck(s) you want to own on the listed deck repository
	- It has a deck repository in which you can create, edit and delete decks
	- It has a card manager that will let you choose as many cards on the listed card repository
	- It has a card repository in which you can create, edit and delete cards
	- It has a skill repository in which you can create, edit and delete skills
	
Programmers Notes:

	- This is only a prototype version of the application in compliance of the final exam of United. 
	- There are still bugs that is in need for a workaround, but so far most of its core features are okay.
	- Further development of the application will continue after the exam
	- You may modify dataSource.dbCreate = update (located at <homefolder>/.mycarddeck/app-config.properties) to 
	  experiment on how the grails and hibernate modifies your tables
