# Lab Report 3
---
## find command
## -size n
-size tells you the kb size of a file . 
"+" indiciates files that are larger than the size that 
"-" indicates files less than that. 
```
$ find ./technical -size +500
./technical/government/Gen_Account_Office/Statements_Feb28-1997_volume.txt
./technical/government/Gen_Account_Office/d01591sp.txt
./technical/911report/chapter-13.4.txt
./technical/911report/chapter-13.5.tx
```
Gets a file that's a size of at least 500 bytes
Helpful for filtering out smaller files 
```
$ find ./technical -size 100
./technical/biomed/1471-2377-3-4.txt
./technical/biomed/gb-2003-4-6-r39.txt
./technical/biomed/gb-2003-4-3-r20.txt
```
This gets files at 100 bytes
helps filters files with the same amount of storage

## -iname n
The -iname  specifies a name of a file to look for 
files with the same format/name will be returned. [command](https://www.tutorialspoint.com/unix_commands/find.htm).

```
$ find ./technical -iname CHAPTER-1.txt
./technical/911report/chapter-1.txt
```
Here it's getting files with the same name but call capital letters 
This helps when trying to look for non case sensitive files.

```
$ find ./technical -iname prEfAcE.txt
./technical/911/report/preface.txt
```

Same lettering but different capitalization
helpful when typing too quickly/typos

## -type n
-type specifies files of a specific type for example, d for directory or f for plain text.
An error will occur when that file does not exist.
[command](https://www.softwaretestinghelp.com/find-command-in-unix/)

```
$ find ./technical -type d
./technical
./technical/government
./technical/government/About_LSC
./technical/government/Env_Prot_Agen
./technical/government/Alcohol_Problems
./technical/government/Gen_Account_Office
./technical/government/Post_Rate_Comm
./technical/government/Media
./technical/plos
./technical/biomed
./technical/911report
```

Helpful when you want to list all possible paths a file could be in.
```
$ find ./technical -type f
... a bunch of lines ...
./technical/911report/chapter-9.txt
./technical/911report/chapter-8.txt
./technical/911report/preface.txt
./technical/911report/chapter-12.txt
./technical/911report/chapter-10.txt
./technical/911report/chapter-11.txt
```
Gets all .txt files
helpful because it lists everything without extra lines
## -o
 -o allows multiple searches together. 
[command](https://unix.stackexchange.com/questions/50612/how-to-combine-2-name-conditions-in-find)
```
$ find ./technical \( -name "chapter-10.txt" -o -name "chapter-9.txt" \)
./technical/911report/chapter-9.txt
./technical/911report/chapter-10.txt
```
Compare two different file names
Helpful when finding similar files
```
$ find ./technical \( -size 80 -o -size +300 \)
./technical/government/About_LSC/commission_report.txt
./technical/government/Env_Prot_Agen/multi102902.txt
./technical/government/Env_Prot_Agen/bill.txt
./technical/government/Env_Prot_Agen/tech_adden.txt
./technical/government/Gen_Account_Office/GovernmentAuditingStandards_yb2002ed.txt
./technical/government/Gen_Account_Office/Statements_Feb28-1997_volume.txt
./technical/government/Gen_Account_Office/pe1019.txt
./technical/government/Gen_Account_Office/d01591sp.txt
./technical/biomed/1471-2164-4-21.txt
./technical/biomed/1471-2091-3-18.txt
./technical/biomed/1472-6785-2-7.txt
./technical/911report/chapter-13.4.txt
./technical/911report/chapter-13.5.txt
./technical/911report/chapter-3.txt
```
Compares two file sizes 
Helps to find out which files to use for specific sizes.
