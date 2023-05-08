Download Link: https://assignmentchef.com/product/solved-swen221-lab-2-exceptions
<br>
The primary purpose of this lab is to get used to working with exceptions. In this lab, you will be working with a very simple database implementation. The database reads data from files stored in a particular plain text format, and then allows that data to be accessed from memory. An example database file is:

ID:int*,Name:str,Age:int

1,John,88

2,Amy,12

3,Sophie,28

4,John,23

The first line of the file describes the database “schema”. That is, the layout which the remaining lines must follow. This includes the number of items which must be provided on each line, along with their permitted type (either an Integer or a String). The asterisk indicates which is the “key field” for the database. This is a special field which uniquely identifies each row such that no two rows may have the same value for the key field, though they can for other fields (e.g. as for the two johns above).

<h2>Getting Started</h2>

To get started, download the file database.jar from course website. This contains the following files:

swen221/database/io/DatabaseFileReader.java swen221/database/lang/ColumnType.java swen221/database/lang/RowType.java swen221/database/lang/Database.java swen221/database/testing/DatabaseTests.java

You should import these files into Eclipse. Note, you will find that they do not compile properly yet.

<h2>Activity 1 — Adding Exceptions</h2>

The first part of the lab is to create the missing classes InvalidRowException, InvalidKeyException and DuplicateKeyException in the package swen221.database.lang. Having correctly created these classes, you should find that the code now successfully compiles. However, it will not yet pass any tests.

<h2>Activity 2 — Reading Database Files</h2>

The second part of the lab is to complete method DatabaseFileReader.findKeyField(). To do this, you might find the methods String.split() and String.endsWith() helpful. Having done this, you may now find the first test is passing (though this depends exactly on how you’ve implemented it).

<h2>Activity 3 — Implementing Database</h2>

The third part of the lab is to construct a class DatabaseImpl which implements the Database interface. You should update method DatabaseFileReader.read() to return an appropriate instance of DatabaseImpl. You will also need to implement all methods from the Database interface correctly. Having done this, you should find that all tests now pass.

<strong>*</strong>