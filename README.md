# Database_Design_Project
MySQL Workbench used to create a database from zero for a company of private trainers on software education, the company is made of software instructors who deliver training services to emerging tech companies.

## FIRST PHASE OF THE PROJECT

I created the first draft EER DIAGRAM based on the analysis of the business. This is a ficticious case study to create an organic and scalable database design. 
It is a first model it is going to be updated later.
It is a software training company, I named it TECHLEARN SOLUTIONS, company of trainers offer live courses/training to tech companies onsite or online and they need a database to handle their business. 

I started off by thinking of the most important tables for this database and the relationships: 

This is my first draft of proposal of the DATABASE DESIGN: 


  ### Company description and solution proposal
'TechLearn Solutions' specializes in providing customized software training programs to 
businesses across various industries. They offer a wide range of training modules covering 
popular programming languages, development frameworks, and software tools. Instructors 
deliver both in-person and virtual training sessions to meet the specific needs and goals of their 
clients.
This database was built with the purpose of efficiently managing their training programs and 
ensure a seamless business experience. Our commitment is to build a robust database system 
that efficiently manages their trainers, clients, and training programs. This centralized hub 
organizes course offerings, pricing, maintains trainer and client details, and tracking training 
sessions. 

Business Rules:
1. Each training course is identified by a unique CourseID and is associated with a specific 
Trainer and Topic.
2. Companies are the clients, they have a contact person representing them and their 
company email address, phone number and Company ID serves as their unique 
identifier.
3. Training sessions can be conducted in-person at the client's location or virtually through 
online platforms.
4. Packages of service differ in price based on how many people are receiving the live or in 
person training, pre-set packages of price are available for different client’s needs.
Entities and Attributes:
1. Company: (CLIENT)
CompanyID (Primary Key): Unique identifier for each company (Integer).
CompanyName:Name of the company (String).
Industry: Industry to which the company belongs (String).
Contact_name: Name of the contact person within the company (String).
Contact_email: Email address of the contact person (String).
Contact_phone: Phone number of the contact person (String).
2. Course:
CourseID (Primary Key): Unique identifier for each course (Integer).
CourseName: Name of the software training course (String).
Course_desription: Description of the course content (String).
Duration: Duration of the course in hours or days (Integer).
Level: Skill level of the course (Beginner, Intermediate, Advanced - String).
3. Trainer:
TrainerID (Primary Key): Unique identifier for each trainer (Integer).
FirstName: First name of the trainer (String).
LastName: Last name of the trainer (String).
Expertise: Area of expertise of the trainer (String).
Email: Email address of the trainer (String).
Phone: Phone number of the trainer (String).
4. Training_session:
SessionID (Primary Key): Unique identifier for each training session (Integer).
CompanyID (Foreign Key): Reference to the company receiving the training (Integer).
CourseID (Foreign Key): Reference to the training course being conducted (Integer).
TrainerID (Foreign Key): Reference to the trainer conducting the session (Integer).
StartDate: Date when the training session starts (Date).
EndDate: Date when the training session ends (Date).
5. Package:
Package_id (Primary Key) Unique identifier for each package (Integer).
Package_price: cost of package (decimal (7,4)
Relationships:
- Company - TrainingSession (One-to-Many): One company can have multiple training 
sessions.
- Course - TrainingSession (One-to-Many): One course can be offered in multiple training 
sessions.
- Trainer - TrainingSession (One-to-Many): One trainer can conduct multiple training 
sessions.
- TrainingSession - Company (Many-to-One): Many training sessions can be conducted 
for one company.
- TrainingSession - Course (Many-to-One): Many training sessions can include one 
course.
- TrainingSession - Trainer (Many-to-One): Many training sessions can be conducted by 
one trainer

EER DIAGRAM
![image](https://github.com/kalejcamto/Database_Design_Project/assets/101201140/792bc1a6-ccf5-4c4e-af8a-d51fe092aab3)

## SECOND PHASE OF THE PROJECT

-  Creating data for the tables in excel and save them as CSV file.
-  ![image](https://github.com/kalejcamto/Database_Design_Project/assets/101201140/836be979-48c9-4153-bb5a-2ca973422653)

-  Forward engineering the import of the EER Diagram into MySQL WORKBENCH TABLES
-  https://github.com/kalejcamto/Database_Design_Project/assets/101201140/c26f0f31-7b23-4d08-9017-a8bd489b6fd9

-  Importing my data sets into the tables using right clic on the table and then clic "Table Data Import Wizard".
-  

## THIRD AND FINAL PHASE OF THE PROJECT
-  Creating at least 8 SELECT queries on the tables.
-  /*TO BE CONTINUE, CURRENTLY WORKINGN ON THIS, AS OF 11/21/23*/
