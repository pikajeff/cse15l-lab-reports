# Lab Report 1 - Remote Access and FileSystem (Week 1)
1. `cd`
- **no arguments** <br/>
![Image](cdNoArg.png) <br/>
working directory: `/c/Users/sanka/lecture1` <br/>
'cd' with no argument has no specific directory to go into, and takes us to the home directory, or `~` by default. <br/>
There was no error.
- **path to directory** <br/>
![Image](cdDir.png) <br/>
working directory: `/c/Users/sanka/lecture1` <br/>
The `cd` command with specified directory `messages` takes us into the `messages` directory as shown in the image. The current directory now is `/c/Users/sanka/lecture1/messages`. <br/>
There was no error. <br/>
- **path to file** <br/>
![Image](cdFile.png) <br/>
working directory: `/c/Users/sanka/lecture1` <br/>
The `Hello.java` file doesm't contain any other files within itself (it's not a directory), so we cannot 'go' inside of it. This command therefore gives an error. <br/>
There was an error. `cd Hello.java` gives an error because the argument is not a directory that we can enter. <br/>
2. `ls` <br/>
- **no arguments** <br/>
![Image](lsNoArg.png) <br/>
working directory: `/c/Users/sanka/lecture1` <br/>
`ls` command with no argument just diplays the contents of the working directory, so `lecture1`. <br/>
There was no error. <br/>
- **path to directory** <br/>
![Image](lsDir.png) <br/>
working directory: `/c/Users/sanka/lecture1` <br/>
`ls messages` with a directory as an argument outputs the contents of the specified directory, in this case, `messages`. As a side note, If I tried to ls a directory *outside* the current directory, it would throw an error. <br/>
There was no error. <br/>
- **path to file** <br/>
![Image](lsFile.png) <br/>
working directory: `/c/Users/sanka/lecture1` <br/>
`ls Hello.java` just outputs the name of the file "Hello.java" as it is not a directory that contains other files within itself. <br/>
There was no error. <br/>
3. `cat` <br/>
- **no arguments** <br/>
![Image](catNoArg.png) <br/>
working directory: `/c/Users/sanka/lecture1` <br/>
`cat ` with no argument just waits for the user to type in something, and then, (This is not shown in the image above) prints out the same input. The terminal just waits for user input, and doesn't give out an immediate output, as shown in the image. <br/>
This does not give an error. <br/>
- **path to directory** <br/>
![Image](catDir.png) <br/>
working directory: `/c/Users/sanka/lecture1` <br/>
`cat messages` doesn't print out the contents within the directory because it is simply a container of different files/directories, and isn't a file that contains text. The output just reinforces that messages is a directory that cannot be 'printed' <br/>
The output is an error that tells us that the argument cannot be a directory. <br/>
- **path to file** <br/>
![Image](catFile.png) <br/>
working directory: `/c/Users/sanka/lecture1` <br/>
`cat Hello.java` prints out the contents of the Hello.java file contained within the current working directory. <br/>
There is no specific error. <br/>

