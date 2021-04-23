# Select Multiple Rows in Table and Pass Row Values to Backend using Ajax & JavaScript.


This POC illustrates how to pass multiple records to a table from one page to another page in the form of array using JavaScript and Ajax. Job applicant data is taken and stored in the form of table. In every record their will be unique value for that particular record, that unique value is taken and stored in JavaScript array. Then this array of unique data is passed in to the backend with the help of ajax for the further use of multiple record Updation or deletion in database.

**Steps to select multiple rows in the table and pass the row values to backend using Ajax & JavaScript are:**

1.	First, create a table and store the required data into the table. 

2.	Below code illustrates how to create and insert values into the respective table.
   
     ![Alt text](https://github.com/Protontech-1803/Web-Technology/blob/main/Transfer%20Multiple%20Records%20to%20Backend/ImagePNG/1.png)

 

  Output of the above code:
  
   ![Alt text](https://github.com/Protontech-1803/Web-Technology/blob/main/Transfer%20Multiple%20Records%20to%20Backend/ImagePNG/2.png)

 
3.	Select the required records using checkbox and click on Check Data to trigger the JavaScript function to filter the selected applicant’s data in a table.

     ![Alt text](https://github.com/Protontech-1803/Web-Technology/blob/main/Transfer%20Multiple%20Records%20to%20Backend/ImagePNG/3.png)

4.	On execution of JavaScript function, array is created to store the selected applicant’s data and filtering is done with the help of for loop to identify the selected record.


5.	As show below when the selected record is found, the record will be pushed into the respective array.

     ![Alt text](https://github.com/Protontech-1803/Web-Technology/blob/main/Transfer%20Multiple%20Records%20to%20Backend/ImagePNG/4.png) 
 

6.	When the applicant’s data is stored in an array, array is converted into json object and passed it to the backend using Ajax XmlHttpRequest. 

     ![Alt text](https://github.com/Protontech-1803/Web-Technology/blob/main/Transfer%20Multiple%20Records%20to%20Backend/ImagePNG/5.png)

7.	In the backend data source, the transmitted json object is decoded into the array for subsequent Updation or Deletion of record in the data source.

