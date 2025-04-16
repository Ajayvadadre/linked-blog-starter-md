Proposed Timeline for Vidyakul Sticky and Customer Check Project
### Phase 1: Understanding Requirements & Setup
Need to go through the services related to IVR flow → 120 mins
-- analyzing single IVR flow → 50 mins
-- understanding post multiple IVR flow → 120 mins
Understand Call Flow → 45 mins 
Understanding API Requirements → 35 mins
Review Customer Check API→ 30 mins
Understanding implementation of response Logic → 60 mins
Understand Sticky Agent API & Mapping → 45 mins
Review Retry Logic, Failover, and Configurations → 65 mins
Validate LSQ agent mapping rules → 50 mins

### Phase 2: UI and IVR Configuration
Going through the UI code of existing feature → 120 mins
-- Verify if the feature and its related components are present in the system→ 50 mins
-- Test if the existing feature works correctly; if not, identify and resolve the issues→ 50 mins
Understanding how to add new strategy for API handler→ 60 mins
Setup IVR & supporting UI Strategy → 120 mins
Making changes in the UI to add the new graph parameter based on the API call and their response
-- API for customer method (paid/unpaid) → 95 mins
-- API status (fail/success) → 65 mins
-- API for sticky agent routing → 65 mins
Analyzing code to add Customer Check API  → 55 mins
Add logic after welcome to trigger Customer Check API in NewInbound service → 95 mins
Implement UI validation for API response fields → 90 mins
Modify UI to support GET_JSON with query parameters → 95 mins
Understanding potential Impacts on Existing UI Flows due to New Parameters - 75 mins
URL construction logic based on UI input → 120 mins

### Phase 3: API Handling & Logic Implementation
Customer Check API
Understanding code flow of NewInboundPrototype service 
-- Understanding the code of existing APIs → 65 mins
-- Analyzing API handling → 65 mins
Build API request logic
-- implement parameter handling → 65 mins
-- implement validation handling → 70 mins
-- implement error handling → 65 mins
-- implement response handling → 80 mins
Handle different response stages (Paid/Unpaid Logic)
-- if the customer paid --> redirect to support team → 65 mins
-- rendering UI on the basis of response → 35 mins
-- if the customer unpaid -->
-- taking decision on sticky API → 65 mins
-- need to send the customer number to LSQ → 50 mins
-- handling the response from the LSQ team → 65 mins
Configure retry logic (up to 3 attempts, 3-sec interval) → 80 mins
Failover logic (route to Paid queue if API fails) → 95 mins
Analyzing code flow of Sticky Agent → 45 mins
Understand flow of  NewInboundPrototype sending a call to InboundPrototype service for agent patching → 80 mins
Understanding the code of existing APIs → 80 mins
Build API call for sticky agent
-- implement parameter handling → 65 mins
-- implement validation handling → 70 mins
-- implement error handling → 65 mins
-- implement response handling → 80 mins
Handling sticky agent API success
-- routing the customer to the number retrieved in API response → 65 mins
Handle fallback if Sticky Agent unavailable
-- need to route the call to default mapped campaign-process → 65 mins
Failover to default campaign-process if Sticky API fails → 65 mins
### Phase 4: Logging & Error Handling
Generate API Logs for Success, Retry, Failure (Both APIs) → 95 mins
Implement Configurable Retry Interval/Attempts → 85 mins
Error response handling and fallback routing → 85 mins
If found any issue with the client's API or existing API (debug and resolve) → 80 mins
Buffer → 70 mins


 
 Grand total:-  3800min, 8days