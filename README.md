# Solutions to the tasks

##### Contributed by : Adhiksha Thorat

### Task 1

Github repository link: https://github.com/ADHIKSHA/Timezone_to_UTC

### Task 2

Github repository link: https://github.com/ADHIKSHA/python_code

### Task 3
These are the steps that I would follow to troubleshoot this situation : 
1. Firstly run the ping command in the terminal to check if the problem is with the website I am trying to access or with my ISP or with my laptop. Use this command `ping 8.8.8.8`, if request times out then, there might be some problem with the internet connection. If the ping is successful but still that particular website cannot be accessed then, the problem is with that website.
2. If the problem is with the internet connection then follow these steps. Type the command `ip link show` to check the network devices that are connected to the machine.
If you are trying to connect to the internet through an Ethernet connection, you must find an entry with the label "eth0" or something starting with "en" . If the status of that device is DOWN then run the command`ip link set eth0 up` to try and switch on the Ethernet connection.
Again enter the command `ip link show`. If a new entry with label "eth0" is found with UP as the status then, the connection has been re-established. If no such entry was found or the status says DOWN then move to step 3.
3. If the internet connection is still not working, then again run the command `ip addr` and check the IP address displayed of the connection I want to connect to. The IP address of the connection is displayed infront of the label 'inet' under the device name. If the IP address shown is different from the connection's IP address then, we need to configure the network's IP address. 
Considering the network's IP address to be : 192.168.2.10.
Then run the command, `ip addr add 192.168.2.10 dev eth0`.
4. If the internet connection is still not working, then I would check if my Antivirus(if present) is blocking the internet connection. I would disable my antivirus and re-try connecting to the internet.
5. I would check my Network manager and all the connections listed to the devices. I would use the Network Manager GUI or the CLI to add,delete or modify the connections to the device I want to connect to. Use commands :\
 `nmcli dev status`\
 `nmcli connection show`\
 Then we can modify the present connections or add new connections to the present connections using the `nmcli` commands. 
6. Finally, I would check the LAN cables coming from the ISP to the router or my machine. Check if the router is configured properly. Plug in any loose wires.
7. If nothing works, I would contact my ISP.


### Task 4
These are steps to update the fork :

1. Clone your remote fork of the repository to your local machine.\
`> git clone git@foo.bar/user/project`

2. Go to the project directory in the CMD.\
`> cd project`

3. Add a remote link to the original repository, named upstream.\
`> git remote add upstream git@foo.bar/project/project`

4. Check for all the exisiting remote links present in your local github repository.\
`> git remote -v`

   ** If you don't already have a remote link to your fork of the repository then, create a remote link called origin by using the following command. \
`> git remote add origin git@foo.bar/user/project`

5. Fetch the current state of the original repository into your local repository.\
`> git fetch upstream`

6. Merge the changes present between your local repository and the original repository. Here 'main' is the branch which needs to be merged with.\
`> git merge upstream/main`

7. Push all the changes to your fork of the repository. This command will successfully help you to sync your fork of the repository to the original repository.\
`> git push origin main`


