1. The very first step is installing visual studio codes. This program is a very simple program that we may use to code many things. 
Downloading is very simple as you search it online and they give you a good instructions on how to install.

https://code.visualstudio.com/

![Image](https://github.com/JamieWei21/cse15l-lab-reports/blob/main/VSC-LabR1.PNG)



2.The next step is to connect to the virtual computer. Go into your visual studio code and open up a new terminal in the top task bar. 
In the terminal type ssh and find your username account on the lookup. Afterwards, put 

Ssh yourusername@ieng6.ucsd.edu

Then you must enter your password which will not be shown on the terminal. This should be enough to get your to login.

![Image](https://github.com/JamieWei21/cse15l-lab-reports/blob/main/Example2-LabR1.PNG)


3. Next step is a simple step. Enter some commands and get used to the new terminal. Enter “ls” “cd” and then try running “exit”.

Ls- shows the list of directory's that you can specifiy into
cd- when entered you enter that changes your path


![Image](https://github.com/JamieWei21/cse15l-lab-reports/blob/main/Example3-labR1.PNG)

4. Next you will find a file called WhereAmI.java compile and run it in your normal terminal. 
Then hop onto the ssh and login to the virtual machine and then type

	Scp (filename) accountname@ieng6.ucsd.edu

![Image](https://github.com/JamieWei21/cse15l-lab-reports/blob/main/Example4-LabR1.PNG)

5. Next we try to set up an SSH key to skip the login. First type in

Ssh-keygen 

Into your normal terminal. It will ask a bunch of questions that you can autofill by pressing enter. 
Next login to the virtual machine via ssh. Next we will use the scp function, type

Scp (location of the keygen that you automatically created in the previous step) accountname@ieng6.ucsd.edu

The location of the keygen is normally stored into the user's .ssh directory under the home directory. 


![Image](https://github.com/JamieWei21/cse15l-lab-reports/blob/main/Example5-LabR1.PNG)


6. The keygen speeds up your ability to login due to being able to skip the password. Passwords aren't shown therefore, the user are blind when typing
their password. It is very unfriendly design and it makes the login more efficient if you have an automatic login. However, due to difficulty when logging into
SSH, I wasn't able to test out this intovation. 


