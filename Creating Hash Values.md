# Creating Hash Values
<br/>
<h2>Description</h2>

In this lab, we will create and evaluate the hash values for two files. We will use Linux commands to calculate the hash of two files and observe any differences in the hashes produced. Then determine if the files are the same, or different.
<br/>

<h2>Generating hashes for files</h2>
First, we will use the <i>ls</i> command to list the contents of the directory. The output prints two files <b>file1.txt and file2.txt.</b>

<br />
  <p align= "center">
  <br />
<img src="https://i.imgur.com/2VvxsGK.png[/img]" alt="ls for hash values"/>
<br />

Now we use the **cat** command to display the contents of the file1.txt file and file2.txt. As you can see the two outputs seem to be identical. 

<h2>Identical hash values</h2>
Although the hash values appear to be identical we will need to generate the hash for each file to determine if the files are actually different.

<br />
  <p align= "center">
  <br />
<img src="https://i.imgur.com/qDmPkY6.png[/img]" alt="sha256sum value"/>
<br />
    
Use the **sha256sum** command to generate the hash of the file1.txt and file2.txt files. The generated hash value for file1.txt is different from the generated hash value for file2.txt, which indicates that the file contents are not identical.

<h2>Compare hashes</h2>
Using the the <i>sha256sum </i> command again we will generate the hash of the file1.txt and file2.txt files, and send the output to a new file called file1hash and file2hash with the (>>) input.
<br />
  <p align= "center">
  <br />
<img src="https://i.imgur.com/XazQmJd.png[/img]" alt="hash outputs to diff files "/>
 <br />
Now we can see using the cat command that the files were transferred below. 
<br />
  <p align= "center">
  <br />
<img src="https://i.imgur.com/NxUMcla.png[/img]" alt="file transfer completed"/>
<br />
    
<h2>Byte by Byte </h2>
Finally we will input the <b>cmp</b> command to compare the two files byte by byte. If a difference is found, the command reports the byte and line number where the first difference is found.

<br />
  <p align= "center">
  <br />
<img src="https://i.imgur.com/uHHhYD6.png[/img]" alt="file transfer completed"/>
<br />

<h2>Summary</h2>
In conclusion we've listed the contents of the home directory, compared the plain text of the two files presented for hashing, computed the sha256sum hash of the two separate files, and finally compared the hashes provided to identify the differences.
