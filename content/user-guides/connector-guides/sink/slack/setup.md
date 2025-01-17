# Slack

This guide contains information to set up a Slack Sink in Vanus Cloud.

## Introduction

Slack is a cloud-based team collaboration platform that allows users to communicate, share files, and integrate with other tools and services.

With Slack Sink connector in Vanus Cloud, you can easily forward real-time updates to a Slack group chat, allowing your team to stay up-to-date on all events generated by your application.


## Prerequisites

Before forwarding events to Slack, you must have:

- A Slack Account
- A [Vanus Cloud account](https://cloud.vanus.ai)

## Getting Started

**To set up an app for receiving events in your Slack channel:**

### Step 1: Create a Slack App
1. Create an [App on Slack](https://api.slack.com/apps).
   ![](images/1.png)
2. Select From Scratch.
   ![](images/2.png)
3. Set the app name and Workspace.
![](images/3.png)

### Step 2: Create a Incoming Webhook
1. select **Incoming Webhooks** in the sidebar menu.
![img.png](images/4.png)
2. Turn on Webhooks and scroll down and click **Add New Webhook to Workspace** to add new webhook.
![](images/5.png)
3. Select the channel to receive messages.
![img.png](images/6.png)
4. Now copy the webhook URL.
![](images/7.png)

Check out this detailed [**Article**](https://www.vanus.ai/blog/get-your-slack-webhook-url/) on how to get a Slack Webhook URL.

### Step 3: Set up your Connection in Vanus cloud 

1. Log in to your [Vanus](https://cloud.vanus.ai) account and click on **connections**  
![3](images/go%20to%20vanuscloud.png)  

2. Click on **Create Connections**  
![3](images/click%20create%20connection.png)  

3. Name your connection, Choose your source and click next 
![3](images/choose%20source.png) 

4. Click on **Sink** and choose **slack** 
![3](images/choose%20sink.png) 

5. Paste the Webhook URL into the `URL` field. 
![img_2.png](images/8.png) 

6. Click **Next** to continue.  

7. Click on submit to finish the configuration. 
![](images/submit.png)  

8. You've successfully created your Vanus slack sink connection.  
![](images/created.png)  

## Required Data Format

The event data must be JSON format, here a simple message, example:

```json
{
  "data": {
    "subject": "Test",
    "message": "Hello Slack!:wave: This is Sink Slack!"
  }
}
```
