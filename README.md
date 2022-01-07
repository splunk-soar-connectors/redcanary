[comment]: # "Auto-generated SOAR connector documentation"
# Red Canary

Publisher: Red Canary  
Connector Version: 1\.1\.1  
Product Vendor: Red Canary  
Product Name: Red Canary  
Product Version Supported (regex): "\.\*"  
Minimum Product Version: 4\.9\.39220  

Integrates with Red Canary's MDR platform

### Configuration Variables
The below configuration variables are required for this Connector to operate.  These variables are specified when configuring a Red Canary asset in SOAR.

VARIABLE | REQUIRED | TYPE | DESCRIPTION
-------- | -------- | ---- | -----------
**url** |  required  | string | Red Canary instance URL \(ex\. https\://domain\.my\.redcanary\.co\)
**api\_key** |  required  | password | Red Canary API authentication key

### Supported Actions  
[test connectivity](#action-test-connectivity) - Validate the asset configuration for connectivity using supplied configuration  
[on poll](#action-on-poll) - Subscribe to Red Canary detections  
[acknowledge detection](#action-acknowledge-detection) - Acknowledge a Red Canary detection  
[remediate detection](#action-remediate-detection) - Update a detection's remediation state  

## action: 'test connectivity'
Validate the asset configuration for connectivity using supplied configuration

Type: **test**  
Read only: **True**

#### Action Parameters
No parameters are required for this action

#### Action Output
No Output  

## action: 'on poll'
Subscribe to Red Canary detections

Type: **ingest**  
Read only: **True**

#### Action Parameters
No parameters are required for this action

#### Action Output
No Output  

## action: 'acknowledge detection'
Acknowledge a Red Canary detection

Type: **generic**  
Read only: **False**

#### Action Parameters
PARAMETER | REQUIRED | DESCRIPTION | TYPE | CONTAINS
--------- | -------- | ----------- | ---- | --------
**detection\_id** |  required  | Unique Red Canary detection identifier | numeric |  `redcanary detection id` 

#### Action Output
DATA PATH | TYPE | CONTAINS
--------- | ---- | --------
action\_result\.parameter\.detection\_id | numeric |  `redcanary detection id` 
action\_result\.data | string | 
action\_result\.status | string | 
action\_result\.message | string | 
action\_result\.summary | string | 
summary\.total\_objects | numeric | 
summary\.total\_objects\_successful | numeric |   

## action: 'remediate detection'
Update a detection's remediation state

Type: **generic**  
Read only: **False**

#### Action Parameters
PARAMETER | REQUIRED | DESCRIPTION | TYPE | CONTAINS
--------- | -------- | ----------- | ---- | --------
**detection\_id** |  required  | Unique Red Canary detection identifier | numeric |  `redcanary detection id` 
**remediation\_state** |  required  | Way in which the detection was remediated | string | 
**comment** |  optional  | Comment describing the reason why the detection was remediated in this manner | string | 

#### Action Output
DATA PATH | TYPE | CONTAINS
--------- | ---- | --------
action\_result\.parameter\.detection\_id | numeric |  `redcanary detection id` 
action\_result\.parameter\.remediation\_state | string | 
action\_result\.parameter\.comment | string | 
action\_result\.data | string | 
action\_result\.status | string | 
action\_result\.message | string | 
action\_result\.summary | string | 
summary\.total\_objects | numeric | 
summary\.total\_objects\_successful | numeric | 