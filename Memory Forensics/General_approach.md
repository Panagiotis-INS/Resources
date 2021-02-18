# How to approach a Forensics challenge #

## NOTE:This logic is applicable mainly on ctfs and educational challenges (e.g:hack the box) ##

<h2>First things first: What file type or what files do we have to work with:</h2>
The first command that we will use is the

```
file
``` 

command in order to see what filetype we(actually) have because sometimes file extensions can 'lie'<br>
After a good google search about the file we can start working on it<br>
<br>
Types of files and how to work around them:<br>
1. ```mem and vmem ``` files:<br>
  These files are memory or virtual memory files (memory dumps of a system) and work with them with Volatility,Redline,Recall<br>
2. ```doc,docx``` or ```other Microsoft office files that can store and run macros``` :<br>
  Yes these files are especially DANGEROUS and SHOULD NEVER BE OPENED with Microsoft office on a MAIN WINDOWS system<br>
  These files as mentioned can store and run macros<br>
  Macros are VB and VBS scripts that can do whatever VB and VBS does combined with shell or even powershell commands<br>
  We work with these files on Linux with Libre office and analyze them with ```Viper Monkey``` <br>
