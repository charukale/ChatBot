# ChatBot

Project Introduction: This chatbot suggests a clinical user a patient monitor based on her preferred specifications. It provides some options to the user and based on those options, the user inputs his or her preferred specifications. With each question, the chatbot filters the 
availavle momitors in the database according to the user specification and at the end provides the user a list of patient monitors which are suitable for his needs.

Maximum Cyclomatic Complexity for code(excluding testing code):3
Maximum Duplication:0

The project contains a total of 5 controllers. Each controller is responsible for a specific functionality provided by the project.
1. Chatbot controller: responsible for all chatbot related operations. Route:("api/Chatbot")
2. Category controller: allows the user to select any of the provided 3 categories(Screen Size, Portability, Touch Screen availability). Throught this controller, user can directly filter the product based on any of the 3 attributes Route:("api/Category") 
3. CustomerData controller: responsible for the user registration. After the user selects  model, the details of the user can be added to the Customer related database. Route:("api/CustomerData/Registration")
4. SalesRepController: Allows to add the data related to the sales representatives who are specific to a specific city. Route:("api/SalesRep/Registration")
5.MonitorSalesController: through this controller, we can access the customers who are assigned with particular sales representatives. If given a name of a salesRepresentative in the url, list of the customers who are assigned with that salesrep can be obtained.

The project contains a database which consists of five tables.
1.PatientMonitor Table: Consists of data related to the Patient Monitors that are to be selected by the customers.
2.Question Table: Consists of the questions that are asked to the customer
3.CustomerData Table: Consists of data of the registered customers.
4.SalesRep Table: Consists of sales representatives of different cities.
5.PatientSale Table: Consists of Registered users with the assigned salesrep name.

We have a total of 5 controllers, 5 interfaces and the implementation of these 5 interfaces in 5 separate classes. Our project uses the concept of DI containers. A DI Container is a framework to create dependencies and inject them automatically when required. 
It automatically creates objects based on the request and injects them when required. DI Container helps us to manage dependencies within the application in a simple and easy way. We are not directly accessing the implementation classes, the implementation is only 
being accessed through the interfaces. This makes our project adaptable to change. 

We have used MOQ framework in the testing environment, this makes testing easier.
