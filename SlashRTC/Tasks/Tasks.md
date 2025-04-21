🟢=completed
🟡=ongoing 


---
### Task - 32237 (Multiple Issues-Balics2s)🟢
- Department - L3 Dev support 
- Assigned by - Kanishk magare
- Ticket number-  060644
- Client name- Balics2s
- Task assigned-  3/18/25 12:46 PM
- status- completed
- Issue - Failed jobs not getting cleared from Queue increasing Redis memory use
- Findings: 
	1. MongoError jobs are getting re-added again and again without any limit to it that might cause queue to be filled quickly
	2. Once a job fails , its not handled to remove it from the queue, in turn filling up the memory
	3. Only time when job is removed when it gets the state completed
- Possible Solutions: 
	- Need to add the failed jobs again in the queue with a limit, after the limit exceeds the data inside job will be inserted in mongo and job is removed from the queue
- Transfered this issue to Ayush nalawade and he has provided a sol for it.

--- 
### Task - React Native app (PBX softphone)🟢
- Department - CD (Customer Delievers)
- Assigned by - Anay Kachare
- Requirement- Webapp dialer in the form of app
- Solution :
	- Created app in React-native
	- Inside the app used Webview to display the entire webapp in the app when opened
	- Added transitions and some UI changes for seamless integration of the webapp 


---

### Task- 33673 Report issue (TMPW(Eclat))🟢
- Department - L3dev-support
- Assigned by - Ashok solanki
- Only inbound call issue
- Call recording time shown in the CDR report is not correct as per talktime 
- findings:
	- userstate -> call : 11:44:51 to dispose: 11:50:37 -> difference: 00:05:46 which is exact what is shown in the recording, same as time between record start to record end.
- Sol: We have listen to the call recording for the case on **04st** **April 2025** at **04 Apr'25 11:44:51**.  
we have found that the conversation between **05:12 and 05:57** which is **44-45** sec is not available,  
and starts at **05:57** in between conversation.  
  

We also gone through the logs for this particular call and found out that the recording start time and  recording stop time is **05:45,**  
We have not found issue from our side.


### QueuePlayer unable to run issue(TechOps)🟢
- Issue is been caused due to code written inside psl/index.js which is used by another library is of node6 and the node version service is running on is node4 which is not able to understand node6 code in that folder, so we need to downgrade it to lower than node6  
- Steps to solve it:  
    - delete old node_modules run->> rm -rf node_modules  
    - run->>npm install request@2.74.0 request-promise@4.1.1 --save-exact  
    - run->>npm i  
    - go to ->cd node_modules/request/node_modules/tough-cookie/node_modules  
        - delete psl folder(As this is using code above node 6 version) run->>  rm -rf psl  
        - run->> npm install psl@1.1.20 --save-exact  
- do same above step to remove psl folder for request-promise run->>  
    cd node_modules/request-promise/node_modules/tough-cookie/node_modules  
        - delete psl folder(As this is using code above node 6 version) run->>  rm -rf psl  
        - run->> npm install psl@1.1.20 --save-exact  
- restart the server run->> pm2 restart 23 && pm2 logs 23




### Task- 061917 Leadset upload issue in (uat-common)🟢
- Department - L3dev-support
- Assigned by - claimed by self
- Issue - Not able to upload leadset with __ underscore
- Findings:- Skillgroup must be present inside skillgroup menu , or else should be entirely empty
	- It should work if there is __ and if there is no __ main there should be skillgroup 
- Sol:- There was no issue related to underscore, issue was of numbers were masked with ( *** )  due to which leadset was not able to insert and returns notAbleToInsert csv file.
  

---- 


### Task - add lines code lines in main.js 🟡
main.js> add DISABLE_SERVICE line below fetchbashfrommongo>inside if isprojectilepath >inside init func below if(fetch bash from mongo add its below if ) 
commit added 
branchname tracelog

#### node14 services: 
1. recordingscheduler (ajay->changes pushed)
2. thresholdhandler(ajay->changes pushed)
3. userInActivator(ajay->changes pushed)
4. eternalCall(Hamza->changes pushed)
5. eventifierService(Hamza->changes pushed)
6. kibanaQueue(Hamza->changes pushed)
7. leadManager(Hamza->changes pushed)
8. liveMonitorV2(Hamza->changes pushed)
9. reportscheduler (Hamza->changes pushed)
10. elasticQueueClient(anupam->changes pushed)
11. AutoDialling(anupam->changes pushed)
12. ApiLogger(anupam->changes pushed)
13. calculateStats(anupam->changes pushed)
14. cloudAuthserver(anupam->changes pushed)
15. stickyagent not added code


#### node4 services:

1. apiQueueConsumer
2. autoFailedReportGenerator
3. beanQueApi
4. bulkLeadPushListen
5. callEventManager
6. callingApis
7. chatOfferManager
8. chatServer
9. churnLeadQueue
10. clientIntegration
11. environServer
12. heartBeater
13. inboundPrototype
14. liveMonitoringSocketServer
15. newInboundPrototype
16. preCallHandler
17. queueConsumer
18. queuePlayer
19. sftpConnect
20. socketServer
21. stateManagementQueue