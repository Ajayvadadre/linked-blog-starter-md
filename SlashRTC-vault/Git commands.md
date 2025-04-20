- git cherry-pick
	- This command is used to
- git init 
	- To initialise git iniside working directory 
- git add 
	- To add the files to staging / index  
- git diff 
	- To check the difference/changes between branches 
- git commit 
	- Git commit makes a new commit object with the files inside stage and points the branch to that commit 









# Imp Git commands for L3server


### Command to go to node14 services
-  ssh root@192.168.0.50 -p 11522
- l3dev (alias)

### Command to go to node4 services
- su - aamir

### Command to check services in that path 
- pm2 l 

### How to create alias
	1 alias
	2 vim ~/.bashrc (To go inside vim editor)
	3 paste this in editor , alias l3dev='ssh root@192.168.0.50 -p 11522
	4 can now use l3dev instead of whole command to go to root(node14 services) folder

### How to check logs for a service 
- pm2 l  (To check the services in that path )
- pm2 show stateManagementQueue (number/name of that service )
- pm2 log stateManagementQueue (number/name of that service )


### To restart a service 

- pm2 restart cloudAuthServer && pm2 logs cloudAuthServer




- npm install eas, signup eas, configure eas, eas build -androidsdfsdfrandome changes 