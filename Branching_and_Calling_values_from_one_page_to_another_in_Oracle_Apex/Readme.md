# Branching and Calling values from one page to another in Oracle Apex

A branch is an instruction to go to a specific page, procedure, or URL. For example, you can
branch from page 1 to page 2 after page 1 is submitted.

We can use declarative or manually coded options with APEX branches to implement and
manage the flow of our APEX application. The Branches section is part of the Page Processing
column, and in most cases it will be the last stage of the application page ACCEPT phase.

The Following are the steps to implement branching in Oracle apex.

**Creating an application in oracle apex:** Login to Oracle apex workspace and Create a
new application inside App builder. Created Application is shown below.

   ![Alt text](https://github.com/Protontech-1803/Web-Technology/blob/main/Branching_and_Calling_values_from_one_page_to_another_in_Oracle_Apex/R1.png)
   
 **Create a table:** Create a table to store the data, below screenshot shows the creation of table using SQL command with a success message. Created tables will display in Object Browser
 
 ![Alt text](https://github.com/Protontech-1803/Web-Technology/blob/main/Branching_and_Calling_values_from_one_page_to_another_in_Oracle_Apex/R2.png)
 
**Creating First Page (Form page):** 
  - Create a new blank page inside the application
  - Create a new Form region inside body
  - Select Table name which has been created in the previous step. Here it is “EMPLOYEES”.
  - Once the table is selected, all the columns from the table will be fetched automatically and it will display as form fields.
  - Create corresponding page items to provide labels for each column as shown in the screenshot

  ![Alt text](https://github.com/Protontech-1803/Web-Technology/blob/main/Branching_and_Calling_values_from_one_page_to_another_in_Oracle_Apex/R3.png)
  
**Creating a process:** Create a process for the form and provide the PL/SQL code for inserting the values into the table from the form. Table&#39;s associated columns are connected to the corresponding fields.

  ![Alt text](https://github.com/Protontech-1803/Web-Technology/blob/main/Branching_and_Calling_values_from_one_page_to_another_in_Oracle_Apex/R4.png)
  
**Output:** Save and run the form page. Created Employee Form will be displayed, Fill the required fields and click Create, this will create a new Employee and get saved in the Employees table.

  ![Alt text](https://github.com/Protontech-1803/Web-Technology/blob/main/Branching_and_Calling_values_from_one_page_to_another_in_Oracle_Apex/R5.png)
  
  - The below screenshot shows the Employee table data in Object browser. New record has
been added into the Employees table

  ![Alt text](https://github.com/Protontech-1803/Web-Technology/blob/main/Branching_and_Calling_values_from_one_page_to_another_in_Oracle_Apex/R6.png)
  
**Create Second page (Report page):**
  - Create a new blank page inside the application
  - Create a subregion and select type as Interactive Report
  - Select source type as SQL Query and provide SQL query to fetch all the columns from Employees Table.
  - Create a dummy column to link a new page as shown the screenshot.


  ![Alt text](https://github.com/Protontech-1803/Web-Technology/blob/main/Branching_and_Calling_values_from_one_page_to_another_in_Oracle_Apex/R7.png)
  
**Create Third page (View page):**
  - Create a new blank page inside the application
  - Create page items inside a static content region to display details of the selected employee.
  - Provide type as display only for all page items and provide names for each page items as shown below.
  
  ![Alt text](https://github.com/Protontech-1803/Web-Technology/blob/main/Branching_and_Calling_values_from_one_page_to_another_in_Oracle_Apex/R8.png)
  
  - Open Report page and click on created dummy column, Select type as Link. This will allow you to link the item to another page by choosing the page number


  ![Alt text](https://github.com/Protontech-1803/Web-Technology/blob/main/Branching_and_Calling_values_from_one_page_to_another_in_Oracle_Apex/R9.png)
  
  Click on target and provide the page number which has been created in the previous step.
 Provide set items as shown below,
 - Name - Page item names of the view page
 - Value - Column names from report page

This will fetch values from the columns and displayed in the corresponding page items.

  ![Alt text](https://github.com/Protontech-1803/Web-Technology/blob/main/Branching_and_Calling_values_from_one_page_to_another_in_Oracle_Apex/R10.png)

**Output:** save and run the report page, Employee table will be displayed with the data, click on view more link to see the view page.

  ![Alt text](https://github.com/Protontech-1803/Web-Technology/blob/main/Branching_and_Calling_values_from_one_page_to_another_in_Oracle_Apex/R11.png)

  - View more link will redirect to the view page where user can see complete details of the employee. The values have been fetched from the previous page i.e. Report page.
  
  ![Alt text](https://github.com/Protontech-1803/Web-Technology/blob/main/Branching_and_Calling_values_from_one_page_to_another_in_Oracle_Apex/R12.png)
  
  


