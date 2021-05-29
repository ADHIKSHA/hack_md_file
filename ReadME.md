# Solutions to the tasks

### Task 1

Github repository link: https://github.com/ADHIKSHA/Timezone_to_UTC

### Task 2

Github repository link: https://github.com/ADHIKSHA/python_code

### Task 3
These are the steps that I would follow to troubleshoot this situation : 
1. Type the command "ifconfig" to check the network devices that are connected to the machine.
If you are trying to connect to the internet through an Ethernet connection, you must find an entry with the label "eth0". If not found you can run the command "ifconfig eth0 up" to try and switch on the Ethernet connection.
Again enter the command "ifconfig".If a new entry with label "eth0" is found with UP as the status then, the connection has been re-established. If no such entry was found or the status says DOWN then move to step 2.
2. If the internet connection is still not working, then again run the command 'ifconfig' and check the IP address displayed of the connection I want to connect to. The IP address of the connection is displayed infront of the label 'inet addr' under the device name. If the IP address shown is different from the connection's IP address then, we need to configure the network's IP address. 
Considering the network's IP address to be : 192.168.2.10.
Then run the command, 'ifconfig eth0 192.168.2.10'.
3. If the internet connection is still not working, then I would check if my Antivirus(if present) is blocking the internet connection.I would disable my antivirus and re-try connecting to the internet.
4. Finally, I would check the LAN cables coming from the ISP to the router or my machine. Check if the router is configured properly. Plug in any loose wires.
5. If nothing works, I would contact my ISP.


### Task 4
These are steps to update the fork :

1. Clone your remote fork of the repository to your local machine.\
-> git clone git@foo.bar/user/project

2. Go to the project directory in the CMD.\
-> cd project

3. Add a remote link to the original repository, named upstream.\
-> git remote add upstream git@foo.bar/project/project

4. Check for all the exisiting remote links present in your local github repository.\
-> git remote -v

   ** If you don't already have a remote link to your fork of the repository then, create a remote link called origin by using the following command. \
-> git remote add origin git@foo.bar/user/project

5. Fetch the current state of the original repository into your local repository.\
-> git fetch upstream

6. Merge the changes present between your local repository and the original repository. Here 'main' is the branch which needs to be merged with.\
-> git merge upstream/main

7. Push all the changes to your fork of the repository. This command will successfully help you to sync your fork of the repository to the original repository.\
-> git push origin main


