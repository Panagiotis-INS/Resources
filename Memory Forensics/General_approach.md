# How to approach a Forensics challenge #

## NOTE:This logic is applicable mainly on ctfs and educational challenges (e.g:hack the box) ##

<h2>First things first: What file type or what files do we have to work with:</h2>
The first command that we will use is the

```
file
``` 

command in order to see what filetype we(actually) have because sometimes file extensions can 'lie'<br>
After a good google search about the file we can start working on it<br>
<h2>Secondly:</h2>
We try to see if the file is damaged or destroyed by looking at a <b>hexdump</b> and with the 

```
xxd
```
command.If the file has some common bytes with known file types and the data bytes are not destroyed we try to recover it with a hexeditor such as<br>

```
hexedit or GHex
```

<br>
Types of files and how to work around them:<br>
1. <b>mem and vmem</b> files:<br>
  These files are memory or virtual memory files (memory dumps of a system) and work with them with Volatility,Redline,Recall<br>
  # NOTE: The file command will show memory files as 'just' data # <br>
2. <b>doc,docx</b> or <b>other Microsoft office files that can store and run macros</b> :<br>
  Yes these files are especially DANGEROUS and SHOULD NEVER BE OPENED with Microsoft office on a MAIN WINDOWS system<br>
  These files as mentioned can store and run macros<br>
  Macros are VB and VBS scripts that can do whatever VB and VBS does combined with shell or even powershell commands<br>
  We work with these files on Linux with Libre office and analyze them with <b>Viper Monkey</b><br>
  After the analysis we deobfuscate them and find the usage of them and find the payload or the exploitation method that the attacker used
3. <b>ISO and general Disk Images</b>  :We usually mount them and search the files inside them or use

```
testdisk
```

If we think that some important files are deleted and recover them.<br>

4. <b>PCAP and PCAPNG</b>:These files are the heart of the Forensic challenges
