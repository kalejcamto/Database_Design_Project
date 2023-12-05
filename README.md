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
DRAFT: ![image](https://github.com/kalejcamto/Database_Design_Project/assets/101201140/792bc1a6-ccf5-4c4e-af8a-d51fe092aab3)
FINAL EXPORT EER DIAGRAM AFTER CORRECTIONS: 
![image](https://github.com/kalejcamto/Database_Design_Project/assets/101201140/27c619df-1fb7-452b-9a7b-c5ecb3465d4d)


## SECOND PHASE OF THE PROJECT

-  Creating data for the tables in excel and save them as CSV file.
-  ![image](https://github.com/kalejcamto/Database_Design_Project/assets/101201140/836be979-48c9-4153-bb5a-2ca973422653)

-  Forward engineering the import of the EER Diagram into MySQL WORKBENCH TABLES
-  https://github.com/kalejcamto/Database_Design_Project/assets/101201140/c26f0f31-7b23-4d08-9017-a8bd489b6fd9
-  ![image](https://github.com/kalejcamto/Database_Design_Project/assets/101201140/1f9425d2-ac46-4eb7-997e-36ece0a7a73c)
-  ![image](https://github.com/kalejcamto/Database_Design_Project/assets/101201140/19490dbd-c6eb-49d7-89f6-e185bec647a8)



-  Created ficticious data to add into the tables. Made it in Excel and exported each excel file into CSV file.
-  ![image](https://github.com/kalejcamto/Database_Design_Project/assets/101201140/3689022f-6d1b-470f-99be-ded213e164bb)

-  Importing my data sets into the tables using right clic on the table and then clic "Table Data Import Wizard".
-  Following these steps:
-  ![image](https://github.com/kalejcamto/Database_Design_Project/assets/101201140/a1dda735-50a0-4958-a28a-87e898df2c37)


## THIRD AND FINAL PHASE OF THE PROJECT
-  Creating at least 8 SELECT queries on the tables.
-  /*TO BE CONTINUE, CURRENTLY WORKINGN ON THIS, AS OF 11/21/23*/

(continuing...) 
-  Importing CSV DATA FILE
-  1. Right clic "Table Data Import Wizard"
 ![image](https://github.com/kalejcamto/Database_Design_Project/assets/101201140/63adff2d-a17e-428c-8e45-a419111e8022)

-  2. Search table data from csv file and Follow the wizard 
 ![image](https://github.com/kalejcamto/Database_Design_Project/assets/101201140/1fd946aa-1337-4ebc-9980-afe927457196)

-  3. Clic next
 ![image](https://github.com/kalejcamto/Database_Design_Project/assets/101201140/618922cb-6eb5-47f3-b28b-d86a7f41e6e1)

-  4. Double check all the boxes are checked with the right "Column Dest"
 ![image](https://github.com/kalejcamto/Database_Design_Project/assets/101201140/2a18b28f-1950-4fec-ac1f-ae7c0d0a40d5)
 
-  5. Clic Next
 ![image](https://github.com/kalejcamto/Database_Design_Project/assets/101201140/eb9dd19e-0bba-4f91-9382-8acc960a533d)
(another table example)


![image](https://github.com/kalejcamto/Database_Design_Project/assets/101201140/6d23f678-1261-4420-ba3e-15ec03e148fe)

-  6. Last Step clic on "Finish".
 ![image](https://github.com/kalejcamto/Database_Design_Project/assets/101201140/c78dfb7d-85a4-4957-9b44-435599981d1a)

(another table example) 

![image](https://github.com/kalejcamto/Database_Design_Project/assets/101201140/fa132a2a-1bfd-46d3-9a49-37ce57c54a6f)


