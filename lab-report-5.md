# Part 1 – Debugging Scenario

## Original Student Post :

**What environment are you using (computer, operating system, web browser, terminal/editor, and so on)?**

PC Windows Visual Studio Code Terminal

**Detail the symptom you're seeing. Be specific; include both what you're seeing and what you expected to see instead. Screenshots are great, copy-pasted terminal output is also great. Avoid saying “it doesn't work”.**

Struggling on how to compile and run Array Tests.
```

[cs151sp23b1@ieng6-202]:wavelet: 40$ git clone https://github.com/pameza/wavelet.git Cloning into 'wavelet'...
remote: Enumerating objects: 922, done.
remote: Counting objects: 100% (6/6), done.
remote: Compressing objects: 100% (4/4), done.
remote: Total 922 (delta 2), reused 4 (delta 2), pack-reused 916
Receiving objects: 100% (922/922), 20.92 MiB | 19.12 MiB/s, done. Resolving deltas: 100% (289/289), done.
[cs151sp23b1@ieng6-202]:wavelet:41$ javac NumberServer.java NumberServer.java:4: error: cannot find symbol
class Handler implements URLHandler {
symbol: class URLHandler
NumberServer.java:38: error: incompatible types: Handler cannot be converted to URLHandler Server.start(port, new Handler());
Note: Some messages have been simplified; recompile with -Xdiags: verbose to get full output 2 errors
[cs151sp23b1@ieng6-202]::wavelet: 42$ java NumberServer 4000
Error: Could not find or load main class NumberServer
Caused by: java.lang.ClassNotFoundException: NumberServer

```
**Detail the failure-inducing input and context. That might mean any or all of the command you're running, a test case, command-line arguments, working directory, even the last few commands you ran. Do your best to provide as much context as you can.**

I am not sure what to do, I did not change the code at all and followed the directions?



# Part 2 - Reflection

This quarter I learned how to do a bunch of commands that would save me time. For example, grep, wc, bash, etc... These commands that I learned are very efficient when coding and debugging. At first I was struggling and confused on how to use these codes in my assignemnts but slowly incorporating them. I will definitely make sure to use these commands in future coding classes.
