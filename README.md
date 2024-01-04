<h1>Practicing File Update Algos in Python</h1>

<h2>Description</h2>
Updated a file that identifies employees allowed to access restricted patient records by creating a Python algorithm to check if the allow list contains IP addresses that are also identified in the remove list. The remove list identifies employees that must be removed from the allow list. Addresses that were identified from the remove list were removed from the allow list file.<br />


<h2>Languages and Utilities Used</h2>

- <b>Python</b>
- <b>Jupyter Notebook</b> 

<h2>Environments Used </h2>

- <b>Windows 11</b> (22H2)
- <b>Server 2022</b>

<h2>Program walk-through:</h2>

<p align="center">
Open the file that contains the allow list: <br/>
<img src="https://i.imgur.com/7hTcPQj.png" height="80%" width="80%" alt="File Update Algorithm Steps"/>
<p align="center"> 

<p>I opened the text file using the import_file variable, the with keyword, and the open() function with the "r" parameter for read permissions.
</p>

<br />

<p align="center">
<br />
Read the file contents:  <br/>
<img src="https://i.imgur.com/ROhTbVA.png" height="80%" width="80%" alt="File Update Algorithm Steps"/>
<p align="center"> 

<p>I used the .read() method to read the imported file and store it in a variable named ip_addresses. Then I displayed ip_addresses to examine the data in its current format.
</p>

<br />

<p align="center">
<br />
Convert the string into a list:  <br/>
<img src="https://i.imgur.com/otYcL0t.png" height="80%" width="80%" alt="File Update Algorithm Steps"/>
<p align="center"> 

<p>After reading the file, I reassigned the ip_addresses variable so its data type was updated from a string to a list. I used the .split() method to achieve this. Adding this step allowed me to iterate through each of the IP addresses in the allow list instead of navigating a large string that contained all the addresses merged together. Then I displayed the ip_addresses variable to verify that the update took place.
</p> 
<br />

<p align="center">
<br />
Iterate through the remove list:  <br/>
<img src="https://i.imgur.com/evTepph.png" height="80%" width="80%" alt="File Update Algorithm Steps"/>
<p align="center"> 

<p>I removed the elements of remove_list from the ip_addresses list. This required both an iterative statement and a conditional statement. First, I built the iterative statement by naming the loop variable element, looping through ip_addresses, and displaying each element. 
</p>  
<br />

<p align="center">
<br />
Remove IP addresses that are on the remove list:  <br/>
<img src="https://i.imgur.com/rSaFMBV.png" height="80%" width="80%" alt="File Update Algorithm Steps"/>
<p align="center"> 

<p>Here, I built a conditional statement to remove the elements of remove_list from the ip_addresses list. The conditional statement was placed inside the iterative statement that looped through ip_addresses. In every iteration, if the current element in the ip_addresses list was in the remove_list, the remove() method was used to remove that element. Afterwards, I displayed the updated ip_addresses list to verify that the elements of remove_list were no longer in the ip_addresses.
</p>  
<br />

<p align="center">
<br />
Update the file with the revised list of IP addresses:  <br/>
<img src="https://i.imgur.com/YRvxa6I.png" height="80%" width="80%" alt="File Update Algorithm Steps"/>
<p align="center"> 

<p>Finally, I updated the original file that was used to create the ip_addresses list. A line of code containing the .join() method was added to the code so that the file could be updated. This was necessary because ip_addresses must be in string format when used inside the with statement to rewrite the file.
</p>  
<p>The .join() method takes in an iterable (such as a list) and concatenates every element of it into a string. The .join() method is applied to a string consisting of the character that will be used to separate every element in the iterable once its converted into a string. The method is applied to the string " ", which contains just a space character. The argument of the .join() method is  ip_addresses, which was the iterable I wanted to convert. ip_addresses was converted from a list back into a string with a space between each element and the next.
</p>  
<p>Then I built the with statement that rewrote the original file. I used the "w" parameter when calling the open() function to delete the contents in the original file and replaced it with the updated allow list of IP addresses.
</p>  
<br />


<br />
<p align="center"> 
Summary:  <br/>
<p>Python offers various functions and syntax for importing and parsing text files. The with statement allowed me to efficiently open and close the allow list and remove list files. The open() function imported the allow list file by using the file name and “r” to indicate the intent to read the file. The.read() method reads in a file, while the.write() method appends or writes to a file. The for loop iterated over the allow list, while the if statement checked if any of the values from the remove list were in the allow list and removed them from the allow list. The.split() method converted the string to a list to allow Python to compare the contents of the text file against elements of a list.
</p>

<br />
 
</p>


<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
