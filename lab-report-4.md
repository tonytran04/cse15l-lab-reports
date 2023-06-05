# Lab Report 4
---
# 1. Log into ieng6

```
<up><enter><command-v><enter>
```
![image](https://github.com/tonytran04/cse15l-lab-reports/assets/110417599/a7de569e-8c4e-4524-89c2-fb0628894ce1)

![image](https://github.com/tonytran04/cse15l-lab-reports/assets/110417599/5e9ac6ba-2bf3-482e-88ae-5c57606a4fe1)

I login by ssh my cse15L account then I copy pasted my account password to login by pressing cmd+v.

# 2. Clone the fork of the repository
clone the repository by typing the command
```
git clone " "
```
```
[cs15lsp23bl@ieng6-201]:~:58$ git clone https://github.com/tonytran04/lab7.git Cloning into 'lab7'.
remote: Enumerating objects: 55, done.
remote: Counting objects: 100% (20/20), done.
remote: Compressing objects: 100% (16/16), done.
remote: Total 55 (delta 8), reused 12 (delta 4), pack-reused 35
Receiving objects: 100% (55/55), 376.53 KiB | 1.78 MiB/s, done. Resolving deltas: 100% (20/20), done.

```

# 3. Run the failed test
```
cd l<tab><enter>
```
```
bash t<tab><enter>
```
```

[cs15lsp23bl@ieng6-201]:~:59$ cd lab7/ [cs15lsp23bl@ieng6-201]: lab7:60$ bash test.sh
JUnit version 4.13.2
..E
Time: 0.521
There was 1 failure:
1) testMerge2 (ListExamplesTests)
org.junit.runners.model.TestTimedOutException: test timed out after 500 milliseconds
at ListExamples.merge(ListExamples.java:44)
at ListExamplesTests.testMerge2 (ListExamplesTests.java:19)
FAILURES!!!
Tests run: 2, Failures: 1
[cs15lsp23bl@ieng6-201]: lab7:61$
```
By utilizing "cd l + tab," I  navigated to the lab7 directory Similarly, executing "bash t + tab" promptly initiated the test.sh file within lab 7, thanks to the autocompletion recognizing it as the only file starting with a "t" 

# 4. Edit the code file 
```
vim L<tab>.<tab><enter>
```
```
43jexi2<esc>:wq<enter>
```

```

while(index1 < list1.size() && index2 < list2.size()) { if(list1.get(index1).compareTo(list2.get(index2))
result.add(list1.get(index1));
< 0) {
index1 += 1;
}
else {
result.add(list2.get(index2));
}
}
index2 += 1;
while(index1 < list1.size()) {
}
result.add(list1.get(index1));
index1 += 1;
while(index2 < list2.size()) {
result.add(list2.get(index2));
// change index1 below to index2 to fix test index2 += 1;
}
return result;
}
}
:wq

```

+ vim L + tab + . + tab allows me to open up ListExamples.java

+ L + tab allows me to autofill to ListExamples  

+ 43j jumps down 43 spaces to the error line 

+ e jumps to the end of the first word with an error

+ x deletes the number there while i2 inserts 2.

+ esc allows for typing 

+ :wq saves the file enter inputs

# 5. Run the tests
```
<up><up><enter>
```
```

[cs15lsp23bl@ieng6-201]:lab7:62$ bash test.sh JUnit version 4.13.2
Time: 0.015
OK (2 tests)
[cs15lsp23bl@ieng6-201]: lab7:63$
```
up arrow twice gets me the command in my history then pressing enter to use the command.

# 6. Commit and push
```
git add .<enter>
```
```
git commit -m "message"<enter>
```
```
git push<enter>
```
```

[cs15lsp23bl@ieng6-201]:lab7:63$ git add
[cs15lsp23bl@ieng6-201]: lab7:64$ git commit -m "d" [main f5757a1] d
Committer: tony <cs15lsp23bl@ieng6-201.ucsd.edu>
Your name and email address were configured automatically based on your username and hostname. Please check that they are accurate. You can suppress this message by setting them explicitly. Run the following command and follow the instructions in your editor to edit your configuration file:
git config --global --edit
After doing this, you may fix the identity used for this commit with:
git commit --amend --reset-author
4 files changed, 1 insertion(+), 1 deletion(-) create mode 100644 ListExamples.class
create mode 100644 ListExamplesTests.class
create mode 100644 StringChecker.class
[cs15lsp23bl@ieng6-201]: lab7:65$ git push
```
* Git add adds all the files to be commited 
* git commit -m "message" prepares the commits for Github
* git push pushes the changes to github

