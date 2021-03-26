# Updating the row from one table to another using static drop down

This POC illustrates how to update a record from one table to another table using JavaScript.
Follow the step to achieve the desired output,
1.	Create the tables with required records. In this example I have used four tables.
•	Students List
•	Waiting List
•	Approved List
•	Rejected List

2.	Create the table of students to update the record as per the status.
  	
    Note: Status means that different tables in a web page.
    
    ![Alt text](https://github.com/Protontech-1803/Web-Technology/blob/main/Updating%20values%20using%20Dropdown/1.jpg)

3.	Select the status from the dropdown for the particular record.
 
    ![Alt text](https://github.com/Protontech-1803/Web-Technology/blob/main/Updating%20values%20using%20Dropdown/2.png)

4.	Once the status is set, the student record has to get submitted using submit button.   

5.	On submit of a record which calls update function along with its two parameters

    a.	1st parameter is to get select tag element’s ID.

    b.	2nd parameter carries the table name.

    ![Alt text](https://github.com/Protontech-1803/Web-Technology/blob/main/Updating%20values%20using%20Dropdown/3.png)
    
6.	With the first parameter we need to fetch the status(table) that record has to get updated.

7.	Below code is used to get the table name which is selected from the dropdown list.

    ![Alt text](https://github.com/Protontech-1803/Web-Technology/blob/main/Updating%20values%20using%20Dropdown/4.png)

8.	Append old record data from the student table to respective table by considering the row index of a record.
 
    ![Alt text](https://github.com/Protontech-1803/Web-Technology/blob/main/Updating%20values%20using%20Dropdown/5.png)

9.	Depending upon the targeted table, drop down list value is assigned.

    ![Alt text](https://github.com/Protontech-1803/Web-Technology/blob/main/Updating%20values%20using%20Dropdown/6.png)


10.	Update the record to respective table that is selected in student dropdown list.

    ![Alt text](https://github.com/Protontech-1803/Web-Technology/blob/main/Updating%20values%20using%20Dropdown/7.png)

11.	Delete the record once it is updated in different table.

    ![Alt text](https://github.com/Protontech-1803/Web-Technology/blob/main/Updating%20values%20using%20Dropdown/8.png)

12.	 View the output of updated tables.
  
   ![Alt text](https://github.com/Protontech-1803/Web-Technology/blob/main/Updating%20values%20using%20Dropdown/9.png)


