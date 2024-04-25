# CSE 15L - LAB REPORT #2 
## Part 1:
**CHAT SERVER JAVA CODE** <br>
![Image](CodeOne.png) <br>
![Image](CodeTwo.png) <br><br>
**ADD-MESSAGE IMPLEMENTATION 1**
![Image](addMessageOne.png) <br>
URL: http://localhost:4000/add-message?s=Hello&user=jpolitz<br>
Method Called: handleRequest<br>
Arguments: URI object representing the URL above.<br>
Changing Values: messages, message, user<br>
Relevant Field Values Before: messages = "", message=null, user=null<br>
Relevant Field Values After: messages = "jpolitz: Hello\n", message=Hello, user=jpolitz<br><br>
**ADD-MESSAGE IMPLEMENTATION 2**
![Image](addMessageTwo.png) <br>
URL: http://localhost:4000/add-message?s=How%20are%20you&user=Sankalp<br>
Method Called: handleRequest<br>
Arguments: URI object for the URL above.<br>
Relevant Field Values Before: messages = "jpolitz: Hello\n", message=Hello, user=jpolitz<br>
Relevant Field Values After: messages = "John: Hello\nSankalp: How are you\n", message=How are you, user=Sankalp<br><br>
## Part 2:
1. <br> ![Image](lsPrivateKey.png) <br>
2. <br> ![Image](lsPublicKey.png) <br>
3. <br> ![Image](iengLogin.png) <br><br>
## Part 3:
Before Labs 2, I was familiar with launching servers on my local machine, but did not know the different techniques to process and manipulate URLS on these web servers to perform different tasks. I learned how to code these servers using URLHandler and URI methods to give the url different functions such as addMessage or increment for instance. Before Lab 3, I knew how to access the ieng6 Remote Server using my laptop terminal, or WSL, but didn't know how to access it directly from VSCode, which is something I learned.  

  

