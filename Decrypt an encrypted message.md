# Decrypt an encrypted message

<h2>Description</h2> 
In this lab, we will complete a series of tasks to obtain instructions for decrypting an encrypted file. We will list the contents of a directory, use Linux commands to revert a classical cipher back to plaintext, decrypt an encrypted file and restore the file to its original state.


<h2>Reading the contents of a file</h2> 
All of the files in my home directory have been encrypted. I will need to use Linux commands to break the Caesar cipher and decrypt the files so that I can read the hidden messages they contain. 
<p align="center">
  <br />
<img src= "https://i.imgur.com/qlmrFcz.png[/img]" alt="listing contents of a file"/>
 <br />
  
As you can see above, we can use the **ls** command to explore the contents of my home directory and read the contents of a file to gain further instructions. 
 <br />
 
  <h2>Hidden File</h2>
Next we will use the <b>cat</b> command to open the <i>README.txt</i> file.
 
<p align="center">
  <br />
<img src= "https://i.imgur.com/Nr6vLF0.png[/img]" alt="hidden file using cat"/>
  The message in the README.txt file advises that the caesar subdirectory contains a hidden file. 
<br />

To decrypt the Caesar cipher it contains, first we start off with changing the director to the Caesar subdirectory using command **cd caesar.** Next we list all files including the hidden ones by entering **ls -a.** The output displays a hidden file with the name <i> .leftShift3. <i/> The (.) period in the beginning of the file lets us know it's hidden. We will use the <i>cat<i/> command again to lsit it's contents.

  <br />
  <p align="center">
  <br />
<img src= "https://i.imgur.com/2uhG7rQ.png[/img]" alt="steps to decrypt"/>

The file displays a scrambled message, but using both the <b>cat</b> and the <b>tr</b> command we can decrypt the code above. The tr command translates text from one set of characters to another, using a mapping. Let's change back to our home directory using the <b>cd ~</b> command. 
<br />

  <h2>Decrypt a file</h2>
  Use the command line shown in the previous output of .leftshift3 to decrypt the encrypted file. Here we will copy and paste: <b>openssl aes-256-cbc -pbkdf2 -a -d -in Q1.encrypted -out Q1.recovered -k ettubrute.</b>

<br />
  <p align="center">
  <br />
<img src= "https://i.imgur.com/CP0FToN.png[/img]" alt="decrypting a message using openssl"
<br/>

Now we use ls to list the contents again. A new file <i>Q1.recovered<i/> appears in the directory. Using the cat command one last time we can reveal the message of this new decrypted file.
<br />

<h2>Summary</h2>
Using basic Linux Bash shell, we listed all hidden files, decrypted a Caesar cipher and decrypted an encrypted file. 


  
