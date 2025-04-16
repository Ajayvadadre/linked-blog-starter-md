- There is a checkbox in the button settings in the BFL instance, need to move that feature into dev-uat branch 

## Reliance 
###  SOP:
	  1 SOP for Chat Reliance Call start and dispose API changes in Param
		  - client wants to send data in params we changed it and send inside body
	  2 click to call API
		- Client wanted to directly call the number instead of copy & paste inside dialler , so we gave them the call button beside the number or clicking on that number link to directly call the number.
		- params for click to call :- agenTptId :agent login id into CRM , customerNumber, tokenId: process id
		  3 



##  Click to call feature 
 - going through the feature 


Test cases:
## 1 Click to dial 

curl --location 'https://iide.slashrtc.in/slashRtc/callingApis/clicktoDial' \
--header 'Content-Type: application/json' \
--data-raw '{
    "agenTptId" : "sanju@slashrtc.com",
    "customerNumber" : "9167053682",
    "tokenId" : "205e6a45ec9ec609aa5ecca7a16a1093"
}'

## 2 CTI POP-UP 
task type : code update 


### React-app workerThread project
- Insert 5 lakh data in db, use 5 workerthreads, when ask to download data from DB use those 5 worker thread 1 lakh data per workerthread and download it. 


4.08 =59%
5.08 =?
6.08 =?2% reduce

