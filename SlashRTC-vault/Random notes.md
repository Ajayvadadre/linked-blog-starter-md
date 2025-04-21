Extra files in ElasticQueueClient 
- applicationLogic>> 
	- messageHandler.js
	- prepareDataToPush.js
- common>>
	- common\amqpHandler.js
	- common\configManager.js
	- common\configValidator.js
	- common\customHashMap.js
	- common\getElasticSearchClient.js
	- common\mongo.js
	- common\mongoHelper.js
	- common\redisWrapper.js
	- common\simpleQueue.js
	- common\utils.js
- config>>>
	- connection.js
	- mongo.js
- lead>>>
	- router.js
- router>>
	- router.js 
- rpc>>>
	- grpcIPC.js
	- ipc.proto
- src>>>
	- centralizeMongoUpdate.script.js







## How to do Zoho phonebridge integration
- zoho provides Oauth2.0 api 
- slashrtc must need a api to connect with zoho
- need to create apis for outbound , inbound calls, call status  

-  zoho provides widget to integrate html,css and js inside the crm 




# Outreach merge

## Outreach Conflict services 
- KibanaQueue
- callingAPIS
- beanQ
- inboundprototype


- [ ] 11-callingAPIS:outreach-dev  
	- Too many conflicts
- [x] 12-beanQ:outreach-dev
	- redis flag 1 conflict doable 
- [ ] 14-inboundprototype:outreach-dev  
	- 5 conflict files
	- CONFLICT (content): Merge conflict in config/conf.js
	Auto-merging lib/esl.js
	Auto-merging lib/helpers/queueEstimate.js
	CONFLICT (content): Merge conflict in lib/helpers/queueEstimate.js
	Auto-merging lib/helpers/voip.js
	CONFLICT (content): Merge conflict in lib/helpers/voip.js
	Auto-merging lib/newAgentRouting.js
	CONFLICT (content): Merge conflict in lib/newAgentRouting.js
	Auto-merging lib/scripts/src/checkCustomerQ.lua
	CONFLICT (content): Merge conflict in lib/scripts/src/checkCustomerQ.lua
	Auto-merging lib/scripts/src/getAgentForDialer.lua
	Automatic merge failed; fix conflicts and then commit the result.






- [x] KibanaQueue:outreach-dev  
	- conflicts 

- [x] 05-recordSERVER:outreach-dev  
- [x] 10-webAPIS:outreach-dev  
- [x] queuePlayer:outreach-dev  
- [x] 17-chatSERVER:outreach-dev  
- [x] 18-apiIntegration:outreach-dev  
- [x] 19-queueConsumer:outreach-dev  
- [x] 20-apiQueueConsumer:outreach-dev  
- [x] 21-callEventManager:outreach-dev  
- [x] 23-liveMonitoringSocketServer:outreach-dev  
- [x] 24-stateManagementQueue:outreach-dev  
- [x] 27-newInbound:outreach-dev  
- [x] 28-environServer:outreach-dev  
- [x] 29-preCallHandler:outreach-dev  
- [x] 31-churnLeadQueue:outreach-dev  
- [x] 22-stateManagementServer:outreach-dev  
	- disposestate.js >>> extra flag on line no 334 
- [x] autoFailedAndRemoteAgentLeg:outreach-dev  
	- no service available
- [x] socketEvent:outreach-dev
	- no service available



## Node14
- Webapp 
	- conflicts
- calleventmanager
	- conflicts/solvable
- outReachThirdParty
	- conflicts
- live monitor no conflicts
- outReachServer
- cloudAuth 



random
## How to handle tasks

- Move all the old code and there features made for them to current dev-uat branch which is the current code running 
- feature specific flag not client specific 
- one team member for UI and one team member for backend working on 1 feature for that client.
	- one team member will create timeline while one is tracing code for that feature on UI
- docs  of every changes made for that feature 
- feature name ->changes made->client name-> index no(1,2)
- dev-uat->dev-sync-> testing-branch(feature specific branch) 
- pull from dev-sync everyday 
- dev-uat is the main branch on which current code is running on   


Thise-