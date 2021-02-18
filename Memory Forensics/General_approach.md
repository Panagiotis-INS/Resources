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
2.
