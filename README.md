# Red Canary

Publisher: Red Canary <br>
Connector Version: 1.1.0 <br>
Product Vendor: Red Canary <br>
Product Name: Red Canary <br>
Minimum Product Version: 4.9.39220

Integrates with Red Canary's MDR platform

### Configuration variables

This table lists the configuration variables required to operate Red Canary. These variables are specified when configuring a Red Canary asset in Splunk SOAR.

VARIABLE | REQUIRED | TYPE | DESCRIPTION
-------- | -------- | ---- | -----------
**url** | required | string | Red Canary instance URL (ex. https://domain.my.redcanary.co) |
**api_key** | required | password | Red Canary API authentication key |
**verify_server_cert** | optional | boolean | Verify server SSL certificate |

### Supported Actions

[test connectivity](#action-test-connectivity) - Validate the asset configuration for connectivity using supplied configuration <br>
[on poll](#action-on-poll) - Subscribe to Red Canary detections <br>
[acknowledge detection](#action-acknowledge-detection) - Acknowledge a Red Canary detection <br>
[remediate detection](#action-remediate-detection) - Update a detection's remediation state

## action: 'test connectivity'

Validate the asset configuration for connectivity using supplied configuration

Type: **test** <br>
Read only: **True**

#### Action Parameters

No parameters are required for this action

#### Action Output

No Output

## action: 'on poll'

Subscribe to Red Canary detections

Type: **ingest** <br>
Read only: **True**

#### Action Parameters

No parameters are required for this action

#### Action Output

No Output

## action: 'acknowledge detection'

Acknowledge a Red Canary detection

Type: **generic** <br>
Read only: **False**

#### Action Parameters

PARAMETER | REQUIRED | DESCRIPTION | TYPE | CONTAINS
--------- | -------- | ----------- | ---- | --------
**detection_id** | required | Unique Red Canary detection identifier | numeric | `redcanary detection id` |

#### Action Output

DATA PATH | TYPE | CONTAINS | EXAMPLE VALUES
--------- | ---- | -------- | --------------
action_result.parameter.detection_id | numeric | `redcanary detection id` | |
action_result.data | string | | |
action_result.status | string | | success failed |
action_result.message | string | | |
action_result.summary | string | | |
summary.total_objects | numeric | | 1 |
summary.total_objects_successful | numeric | | 1 |

## action: 'remediate detection'

Update a detection's remediation state

Type: **generic** <br>
Read only: **False**

#### Action Parameters

PARAMETER | REQUIRED | DESCRIPTION | TYPE | CONTAINS
--------- | -------- | ----------- | ---- | --------
**detection_id** | required | Unique Red Canary detection identifier | numeric | `redcanary detection id` |
**remediation_state** | required | Way in which the detection was remediated | string | |
**comment** | optional | Comment describing the reason why the detection was remediated in this manner | string | |

#### Action Output

DATA PATH | TYPE | CONTAINS | EXAMPLE VALUES
--------- | ---- | -------- | --------------
action_result.parameter.detection_id | numeric | `redcanary detection id` | |
action_result.parameter.remediation_state | string | | |
action_result.parameter.comment | string | | |
action_result.data | string | | |
action_result.status | string | | success failed |
action_result.message | string | | |
action_result.summary | string | | |
summary.total_objects | numeric | | 1 |
summary.total_objects_successful | numeric | | 1 |

______________________________________________________________________

Auto-generated Splunk SOAR Connector documentation.

Copyright 2026 Splunk Inc.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing,
software distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and limitations under the License.
