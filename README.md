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

<p>I opened the text file using the <b>import_file</b> variable, the <b>with</b> keyword, and the <b>open()</b> function with the <b>"r"</b> parameter for read permissions.
</p>

<br />

<p align="center">
<br />
Read the file contents:  <br/>
<img src="https://i.imgur.com/ROhTbVA.png" height="80%" width="80%" alt="File Update Algorithm Steps"/>
<p align="center"> 

<p>I used the <b>.read()</b> method to read the imported file and store it in a variable named <b>ip_addresses</b>. Then I displayed <b>ip_addresses</b> to examine the data in its current format.
</p>

<br />

<p align="center">
<br />
Convert the string into a list:  <br/>
<img src="https://i.imgur.com/otYcL0t.png" height="80%" width="80%" alt="File Update Algorithm Steps"/>
<p align="center"> 

<p>After reading the file, I reassigned the <b>ip_addresses</b> variable so its data type was updated from a string to a list. I used the <b>.split()</b> method to achieve this. Adding this step allowed me to iterate through each of the IP addresses in the allow list instead of navigating a large string that contained all the addresses merged together. Then I displayed the <b>ip_addresses</b> variable to verify that the update took place.
</p> 
<br />

<p align="center">
<br />
Iterate through the remove list:  <br/>
<img src="https://i.imgur.com/evTepph.png" height="80%" width="80%" alt="File Update Algorithm Steps"/>
<p align="center"> 

<p>I removed the elements of <b>remove_list</b> from the ip_addresses list</b>. This required both an iterative statement and a conditional statement. First, I built the iterative statement by naming the loop variable <b>element</b>, looping through <b>ip_addresses</b>, and displaying each<b> element</b>. 
</p>  
<br />

<p align="center">
<br />
Remove IP addresses that are on the remove list:  <br/>
<img src="https://i.imgur.com/rSaFMBV.png" height="80%" width="80%" alt="File Update Algorithm Steps"/>
<p align="center"> 

<p>Here, I built a conditional statement to remove the elements of <b>remove_list</b> from the <b>ip_addresses</b> list. The conditional statement was placed inside the iterative statement that looped through <b>ip_addresses</b>. In every iteration, if the current element in the <b>ip_addresses</b> list was in the <b>remove_list</b>, the <b>remove()</b> method was used to remove that element. Afterwards, I displayed the updated <b>ip_addresses</b> list to verify that the elements of <b>remove_list</b> were no longer in the <b>ip_addresses</b>.
</p>  
<br />

<p align="center">
<br />
Update the file with the revised list of IP addresses:  <br/>
<img src="https://i.imgur.com/YRvxa6I.png" height="80%" width="80%" alt="File Update Algorithm Steps"/>
<p align="center"> 

<p>Finally, I updated the original file that was used to create the <b>ip_addresses</b> list. A line of code containing the <b>.join()</b> method was added to the code so that the file could be updated. This was necessary because <b>ip_addresses</b> must be in string format when used inside the <b>with statement to rewrite the file.
</p>  
<p>The <b>.join()</b> method takes in an iterable (such as a list) and concatenates every element of it into a string. The <b>.join()</b> method is applied to a string consisting of the character that will be used to separate every element in the iterable once its converted into a string. The method is applied to the string " ", which contains just a space character. The argument of the <b>.join()</b> method is <b>ip_addresses</b>, which was the iterable I wanted to convert. <b>ip_addresses</b> was converted from a list back into a string with a space between each element and the next.
</p>  
<p>Then I built the <b>with</b> statement that rewrote the original file. I used the <b>"w"</b> parameter when calling the <b>open()</b> function to delete the contents in the original file and replaced it with the updated allow list of IP addresses.
</p>  
<br />


<br />
<p align="center"> 
Summary:  <br/>
<p>Python offers various functions and syntax for importing and parsing text files. The  <b>with</b> statement allowed me to efficiently open and close the allow list and remove list files. The  <b>open()</b> function imported the allow list file by using the file name and  <b>“r”</b> to indicate the intent to read the file. The  <b>.read()</b> method reads in a file, while the  <b>.write()</b> method appends or writes to a file. The  <b>for</b> loop iterated over the allow list, while the  <b>if</b> statement checked if any of the values from the remove list were in the allow list and removed them from the allow list. The  <b>.split()</b> method converted the string to a list to allow Python to compare the contents of the text file against elements of a list.
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
