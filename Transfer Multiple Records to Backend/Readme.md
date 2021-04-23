# Select Multiple Rows in Table and Pass Row Values to Backend using Ajax & JavaScript.


This POC illustrates how to pass multiple records to a table from one page to another page in the form of array using JavaScript and Ajax. Job applicant data is taken and stored in the form of table. In every record their will be unique value for that particular record, that unique value is taken and stored in JavaScript array. Then this array of unique data is passed in to the backend with the help of ajax for the further use of multiple record Updation or deletion in database.

**Steps to select multiple rows in the table and pass the row values to backend using Ajax & JavaScript are:**

1.	First, create a table and store the required data into the table. 

2.	Below code illustrates how to create and insert values into the respective table.
   
     ![Alt text](https://github.com/Protontech-1803/Web-Technology/blob/main/Transfer%20Multiple%20Records%20to%20Backend/ImagePNG/1.png)

         <!DOCTYPE html>
         <html lang="en">
         <head>
             <meta charset="UTF-8">
             <meta http-equiv="X-UA-Compatible" content="IE=edge">
             <meta name="viewport" content="width=device-width, initial-scale=1.0">
             <link rel="stylesheet" href="..\includes\bootstrap.css">
             <title>Select multiple rows in a table throw checkboxes and pass the row value to the backend using Ajax and Javascript.</title>
         </head>
         <body>

             <table class="table" id="candidate_table">
                 <thead class="thead-dark">
                     <tr>
                         <th scope="col">Serial No.</th>
                         <th scope="col">Select Applicant</th>
                         <th scope="col">Designation</th>
                         <th scope="col">Name</th>
                         <th scope="col">Email</th>
                     </tr>
                 </thead>
                 <tbody>
                     <tr>
                         <td>1</td>
                         <td><input type='checkbox' name='candidates' class='candidates'  value='Steve' style="margin-left: 19%;"></td>
                         <td>Java Developer</td>
                         <td>Steve</td>
                         <td>Steve@fun.com</td>
                     </tr>
                     <tr>
                         <td>2</td>
                         <td><input type='checkbox' name='candidates' class='candidates'  value='Nelson' style="margin-left: 19%;"></td>
                         <td>Java Developer</td>
                         <td>Nelson</td>
                         <td>Nelson@fun.com</td>
                     </tr>
                     <tr>
                         <td>3</td>
                         <td><input type='checkbox' name='candidates' class='candidates'  value='Peter' style="margin-left: 19%;"></td>
                         <td>Java Developer</td>
                         <td>Peter</td>
                         <td>Peter@fun.com</td>
                     </tr>
                     <tr>
                         <td>4</td>
                         <td><input type='checkbox' name='candidates' class='candidates'  value='Anderson' style="margin-left: 19%;"></td>
                         <td>Java Developer</td>
                         <td>Anderson</td>
                         <td>Anderson@fun.com</td>
                     </tr>
                     <tr>
                         <td>5</td>
                         <td><input type='checkbox' name='candidates' class='candidates'  value='Smith' style="margin-left: 19%;"></td>
                         <td>Java Developer</td>
                         <td>Smith</td>
                         <td>Smith@fun.com</td>
                     </tr>
                 </tbody>
             </table>
             <button  onclick="getvalues()" style="margin: 0 auto;display: block;">Check Data</button>
             <script>

             function getvalues(){

                 //create an array to store element values
                 var arr=[];

                 var check=document.getElementsByClassName("candidates");      

                 //push the checkbox checked element value to array
                     for(var i=0;i <check.length;i++){               
                         if(check[i].checked == true)
                         {
                             arr.push(check[i].value);                
                         }
                     }
                     //checking the data of array            
                     alert(arr);
                                         //Send the XMLHttpRequest to pass the data
                                         var ajax= new XMLHttpRequest();
                                 ajax.open('POST','pass.php');
                                 ajax.onreadystatechange = function (){

                                             //If readyState and status condition is satisfied when the data as been passed to backend page successfully
                                    if (ajax.readyState == 4 && ajax.status == 200)
                                       {
                                                 alert(ajax.responseText);                           
                                       }
                                 }
                                 ajax.setRequestHeader("Content-type","application/x-www-form-urlencoded" );
                                         //we need to convert the array to JSON format
                                 ajax.send("delete_candidates="+JSON.stringify(arr));
                                         // In the backend we need to decode Json object(array) to access the data

                                         location.reload();
             }
             </script>
         </body>
         </html>
 

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

