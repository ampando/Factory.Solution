# Silly Stringz INC. 

#### Creating a Web Application, using Many-To-Many database relationships with C# for Epicodus 08.11.2022

### By Adrienne Matosich 

## Description

Another C# independent project! We've attached a database using MySql Workbench and implemented Entity Framework to link it to our application. This factory application is designed to help Dr. Sillystringz keep track of his engineers and thier machine repairs.

## Specifications

**Behavior**: Program will have a homepage where users can choose to view current engineers.
  * Input: User clicks "View Engineers"
  * Output: User is taken to a page with a list of engineers

**Behavior**: Program will have a homepage where users can choose to view current machines.
  * Input: User clicks "View Machines"
  * Output: User is taken to a form to add a new stylist

**Behavior**: Program will allow a user to select an engineer and see what machines that engineer is licensed to repair.
  * Input: User clicks on a specific engineer
  * Output: User is taken to a details page with machines listed

**Behavior**: Program will allow a user to select a machine and see what engineer is licensed to repair that machine.
  * Input: User clicks on a specific engineer
  * Output: User is taken to a details page with engineers listed

 **Behavior**: Program will allow user to add new engineers.
  * Input: User clicks "Add new engineer"
  * Output: User is taken to a page with a form to add another engineer.

**Behavior**: Program will allow user to add new machines.
  * Input: User submits "add new machine"
  * Output: User is taken to a page with a form to add another engineer.

**Behavior**: Program will allow user to edit or delete a engineer/machine.
  * Input: User clicks "Edit/Delete Engineer/Machine"
  * Output: User can change/delete name and/or current Engineer/Machine

**Behavior**: Program will allow user to add machines that an engineer is licensed to repair.
  * Input: User clicks "Add Engineer"
  * Output: User is taken to a page with a form that allows them to add machines for that engineer.

**Behavior**: Program will allow user to add engineers that are licensed to repair a specific machine. 
  * Input: User clicks "Add Machine"
  * Output: User is taken to a page with a form that allow them to add machines for that machine.

## Setup/Installation Requirements

1.  Navigate to the [Factory.Solution repository](https://github.com/ampando/Factory.Solution) or open your terminal

2. Clone this project using the GitHub button or the command:
`$ git clone https://github.com/ampando/Factory.Solution.git`

3. Confirm that MYSQL server is running by opening your terminal and entering the command `mysql -uroot -pepicodus`.

4. Open MySQL Workbench and click on the the `Administration` tab. 

5. Click on `Data Import/Restore` in the left-hand column.

6. Select `Import from Self-Contained File`, and enter the path to adrienne_matosich.sql. An example path could look like this: /Users/yourname/desktop/HairSalon.Solution/adrienne_matosich.sql.

7. Click on the `New` button in the Default Schema to be `Imported To` and for the schema name enter 'adrienne_matosich'.

8. In the drop down menu, select (Dump Structure Only) if you'd like to import only the data structure or (Dump Structure and Data) if you'd like to dump both the structure and data previously entered. 

9. Click the `Start Import` button to finish adding the database.

10. Navigate to the `Factory.Solution` directory in your editor of choice, or use [Visual Studio Code](https://code.visualstudio.com/)

11. Within the project, navigate to the HairSalon.Solution directory, and type `dotnet restore`, then `dotnet build`. Once the build is complete, type `dotnet run` into the terminal. Click on the provided local host link in the terminal to view the web application in your browser.

## SQL Schema Query

The SQL commands below can be used with a the SQL manager to create the database for this project:

DROP DATABASE IF EXISTS `adrienne_matosich`;
CREATE DATABASE `adrienne_matosich`;

USE `adrienne_matosich`;

CREATE TABLE `engineers` (
  `EngineerId` int NOT NULL AUTO_INCREMENT,
  `EngineerName` varchar(255) NOT NULL,
  `ExpierenceLevel` varchar(255) DEFAULT NULL,
  `MachineId` int DEFAULT '0',
  PRIMARY KEY (`EngineerId`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_0900_ai_ci;

CREATE TABLE `machines` (
  `MachineId` int NOT NULL AUTO_INCREMENT,
  `MachineModel` varchar(255) DEFAULT NULL,
  PRIMARY KEY (`MachineId`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_0900_ai_ci;

## appsettings.json

Update your username and password in the appsettings.json file. By default these are set to:
user:root and an [empty password].

## Protecting Your Data

1. In your project's root directory, create an .gitignore file.

2. Add the following to your .gitignore file (this protects your sensitive data).
    DO NOT PROCEED UNTIL YOU COMPLETE THIS STEP!
    * appsettings.json
    * bin/
    * obj/

3. Commit your .gitignore file.

## Known Bugs

The css styling needs more time. 

## Support and Contact Details

If there are any issues or questions, please reach out to me through [my GitHub account](https://github.com/ampando).

## Technologies Used

*  [Visual Studio Code](https://code.visualstudio.com/)
*  [Markdown](https://daringfireball.net/projects/markdown/)
*  [C#](https://docs.microsoft.com/en-us/dotnet/csharp/)
*  [.NET5.0](https://dotnet.microsoft.com/download/dotnet-core/net5.0)
*  [ASP.NET Core MVC](https://docs.microsoft.com/en-us/aspnet/core/mvc/overview?view=aspnetcore-3.1)
*  [Entity FrameWork](https://docs.microsoft.com/en-us/ef/)

### License

*This project uses the following license: [MIT](https://opensource.org/licenses/MIT)*

Copyright(c) 2022  **_Adrienne Matosich_** 