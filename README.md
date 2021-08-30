# RDI.TechChallenge
TechChallenge for RDI Process
Cashless Registration
Version 1.0


This microservice contains 2 APIs:
	1 – API that receive customer card and save it on the db
	2 – API that validate that token based on data provided in the request


NOTE: The framework used to develop this application is compatible with Windows and Unix operating systems.
	
To run this application it´s necessary has MongoDb installed.

If using Windows, MongoDB is installed at C:\Program Files\MongoDB by default. Add C:\Program Files\MongoDB\Server\<version_number>\bin to the Path environment variable. This change enables MongoDB access from anywhere on your development machine.
	Link for download: https://www.mongodb.com/try/download/community?tck=docs_server

If using Unix, run the following commands to install and configurate MongoDb:
	wget -qO - https://www.mongodb.org/static/pgp/server-5.0.asc | sudo apt-key add -
	Create the list file /etc/apt/sources.list.d/mongodb-org-5.0.list for your version of Ubuntu.
	sudo apt-get install -y mongodb-org
	sudo systemctl start mongod


To create database in MongoDb, run MongoDb Shell and run following commands:
	- Use CashlessRegistration
	- db.Card.insertMany([{CardId: 0, CostumerId: 0, CardNumber: 0, CVV: 0, Token: 0, RegistrationDate: "2000-01-01 00:00:00"}])
