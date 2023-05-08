Download Link: https://assignmentchef.com/product/solved-solveddatabase-for-student-solution
<br>
In this task, you are going to develop a database program to store information related to the students of a university. Information to be stored related to a student

Each student record in the database contains the following information.&lt;table&lt;tr&lt;tdName&lt;/td &lt;/tr&lt;tr&lt;tdID&lt;/td &lt;tr&lt;tdCourse&lt;/td e.g. 1612 Master of Computer Studies (cannot be NULL)&lt;/td&lt;/tr&lt;tr1. year (4 digits)&lt;/br2. session (one char A/S for autumn/ spring)&lt;/br3. code (7 characters)&lt;/br4. credit (2 digits, i.e., if the credit point is 6, it will be represented a 06)&lt;/br5. Mark (0 to 100 or e or w)&lt;/bre enrolled, w means withdraw&lt;/brYou may assume each student can be associated with at most 30 subjects&lt;/td&lt;/tr&lt;tr&lt;tdGPA&lt;/td&lt;/table

GPA is defined as:

Sum of {credit of all subjects multiplied by their scores} divided by Sum of {credits of all subjects}All subjects here means subjects that is not of the status e and w.

A sample data file (a plain text file) is given below to illustrate the format.

The ###START### and ###END### are used to mark the starting and ending of the file, while ###RECORD### is used to illustrate the starting of a new record.

![Fig](https://github.com/GoldOne/See-pei-pei/blob/master/fig_bed/sample%20data%20file.png)

Your database program supports the following commands (the should be shown in the first level menu)

**Main Menu**&lt;table&lt;tr&lt;tr&lt;tdq&lt;/td &lt;tr&lt;tdi&lt;/td // the function asks for a file name and import all records from the file&lt;/br// IF record with duplicated ID exists, your program should display the information of both records and ask the user to choose one&lt;/td&lt;/tr&lt;tr&lt;tde&lt;/td // the function asks for a file name and output all records to this file&lt;/br// IF the file already exists, your program should ask if the user would like to overwrite the file or cancel&lt;/td&lt;/tr&lt;tr&lt;tds&lt;/td

You can assume the maximum size of your database is 1000. The import function will take in the maximum allowable records, return to the main menu and display the number of imported records.

**Search Menu**

The following commands are supported in the search menu&lt;table&lt;tr&lt;tr&lt;tdr&lt;/td &lt;tr&lt;tdn&lt;/td the function asks for a name (support one single wild card *)&lt;/br* means everything, e.g. *n means any name that ends with the letter n and that A*n means any name that starts with A and ends with n&lt;/td&lt;/tr&lt;tr&lt;tds&lt;/td return a list of students taking the subject matching the search criteria&lt;/brpromote the user for year, session and code&lt;/brfor each input, the user can use the wild card *&lt;/td&lt;/tr&lt;tr&lt;tdg&lt;/td for =, any result within 1 point of the specified GPA is considered a match&lt;/brThat is, if the user want to search for students with GPA = 5.5, it will display all students whose GPA is from 4.5 to 6.5 (inclusive)&lt;/td&lt;/tr&lt;tr&lt;tdNOTES&lt;/td

**Display Menu**

The following commands are supported in the search menu

&lt;table&lt;tr&lt;tr&lt;tdr&lt;/td &lt;tr&lt;tds&lt;/td &lt;tr&lt;tdn&lt;/td &lt;tr&lt;tdp&lt;/td &lt;tr&lt;tde&lt;/td Upon completion, it shows the old and edited record and ask the user for confirmation.&lt;/brAfter that, it returns to the search menu.&lt;/brFor all options, if the user just press enter, it means keeping the existing value.&lt;/brIf the newly entered ID is not unique, it gives an error and ask the user to re-enter the value.&lt;/td&lt;/tr&lt;tr&lt;tdd&lt;/td Ask the user to confirm the deletion. If confirmed, it deletes the record and return to the main menu.&lt;/td&lt;/tr&lt;/table

**Addtional Menu**&lt;table&lt;tr&lt;tdI&lt;/td&lt;tr&lt;tdE&lt;/tdrequirement is that it has to be compatible with the Import from a binary file function.&lt;/td&lt;/tr&lt;tr&lt;tdC&lt;/tdcourse name. Display the conflicting records and ask the user to choose one of thetwo options:&lt;/br– ignore&lt;/br– all records to one of these conflicting names&lt;/td&lt;/tr&lt;tr&lt;tdO&lt;/td fields: Name, ID and GPA&lt;/brRecords should always be displayed according to the sort key and order.&lt;/brDefault option is shown below:&lt;/brFirst Sort Key: ID , ascending&lt;/brSecond Sort Key: Name, ascending&lt;/brThird Sort Key: GPA, descending&lt;/br&lt;iRemark: it means that records should be ordered according to the first sort key. Ifthey have the same first sort key, they are ordered according to the second sortkey… (For easy implementation, it is possible for the user to set all three sort key tothe same field)&lt;/i&lt;/brRecords should always display according to the setting in this menu.&lt;/td&lt;/tr&lt;/table

All commands are case sensitive. If the user enters an invalid input, your system shouldprompt the user to re-enter. You can assume the user will never enter anything longer than100 characters.





