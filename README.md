# Twilio Serverless Function - Legacy SendToFlex SMS

Twilio Serverless Function mimic for **Legacy Progammable Chat/Proxy Studio *SendToFlex* Widget**

This code performs 3 actions:
1. [Creates a TaskRouter Task](https://www.twilio.com/docs/taskrouter/api/task#create-a-task-resource)
2. [Deletes the Chat Channel Webhook](https://twilio.com/docs/chat/rest/channel-webhook-resource#delete-a-channelwebhook-resource) associated to Studio
3. [Updates the Chat Channel](https://www.twilio.com/docs/chat/rest/channel-resource#update-a-channel-resource) `attributes` with the Task SID created


## environment variables
| Variable | Resource |
| ---- | ---- | 
| WORKSPACE_SID | TaskRouter Workspace SID 
| WORKFLOW_SID | TaskRouter SMS Workflow SID


## studio configuration
In the `Run Function` Widget from the Studio Flow, pass the following key/value pairs to the Serverless Function:

| Variable | Studio Reference |
| ----- | ---- |
| Chat Channel SID | {{trigger.message.ChannelSid}}
| Chat Service SID | {{trigger.message.InstanceSid}}
| Chat Channel Webhook SID | {{trigger.message.WebhookSid}}


## disclaimer
This software is to be considered "sample code", a Type B Deliverable, and is delivered "as-is" to the user. Twilio bears no responsibility to support the use or implementation of this software.
