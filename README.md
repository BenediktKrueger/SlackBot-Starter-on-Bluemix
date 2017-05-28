# Slack bot with various Watson Services from IBM Bluemix implemented in Node Red/ Node.js

This project is an easy starting point for the creation of your first bot using a Messenger like Slack, Facebook or Whatsapp. The beauty about chat bot's is that you not necessarily need to develop an individual mobile or frontent application just to use it. Because there already exists several different Messenger and you can simple use them. 
Used Bluemix Services: Cloudant, Watson Visual Recognition, Watson Natural Language and Watson Conversation. 
The Deployment process is automated with a one-click-Deploy to Bluemix.

## Prerequisites 	
Create a Bluemix account: [Bluemix account] - (Trial Account free for 30 days - no credit card required) <br />
Create a Slack account and create a new team: [Slack registration]	<br />
Create a Slack bot and save the API token: [Slack bot registration]

## One-Click-Deploy to your Bluemix instance 
<br>
<a href="https://bluemix.net/deploy?repository=https://git.ng.bluemix.net/benedikt.krueger/SlackBotRepairExperience"> <img src="https://bluemix.net/deploy/button.png" alt="Deploy to Bluemix"></a>

After you clicked this button you will be redirected to Bluemix and a automated toolchain will clone the repository from git. Moreover is a Bluemix app created, the required services are created and bound to the app.  

## Setup Node Red Flow
1. Click on the deployed Bluemix app in the dashboard and visit app URL. The Node Red application should open now.
2. Go to the Conversation flow (should be default flow) and open the Slack API Input and Output node. Insert Bot API Token (from the Prerequisites).
3. Open the Dashboard by using the link: https://{{YourAppName}}.mybluemix.net/ui and insert your own slack bot api token and direct message channel id (from the Prerequisites). 

Afterwards you can already start using your bot from Slack by ask him some questions. At this point you won't receive an answer because your bot logic was not implemented yet.   
Slack API help and methods: https://api.slack.com/methods

## Implement bot logic by using Watson Conversation Service
1. Open the created Watson conversation service and launch the conversation tool. 
2. Import an existing Conversation example for instance: [default coached conversation] or create your own workspace (help here: [Conversation introduction])  

Now you can really start to ask questions in your slack channel and receive answers based on your implemented bot logic. 

## Analyze bot conversations using Watson Natural Language Understanding
1. Open the ui Dashboard again link: https://{{YourAppName}}.mybluemix.net/ui
2. Click on analyze conversation history and you will receive the most relevant conversation topics, number of messages, sentiments and emotions. 

![Conversation Analytics](http://i.imgur.com/6freuob.png)



Analyzing conversations can be used to extent your bot's capabilities and implement new use cases.  

- - - -

## Next Steps
 * give feedback  
 * integrate other Messenger
    * Facebook
	* Whatsapp
 * more detailed Analytics
 * self extending/ learning conversations
		  

## Common error handling - open the Bluemix log in Case of an error
Restart the browser and application on Bluemix, delete your cache

| Problem description      | Solution    
| :------------- | :--------- |
| Number of Services exceeded       | Delete your used Services or select an empty region or create a new Account. Make sure your account has 5 services available |
| Memory Usage exceeded  | Delete or stop your used Apps or change to an empty space. Make sure your account has 500 mb ram available |
| Cloned repository failure   | There is probably a temporary problem with Bluemix, check the status on: [bluemix status] |
| Dashboard UI is not accessible    | Restart application |
| Deployment Error    | Make sure you delete all services and apps from previous tries |

- - - -

##### Don't hesitate to contact us in case you need additional support - <a href="mailto:benedikt.krueger@de.ibm.com">Benedikt Krüger</a>

[Bluemix account]: https://console.ng.bluemix.net/registration/
[Slack registration]: https://slack.com/signin
[Slack bot registration]: https://my.slack.com/services/new/bot
[general toolchain support]: https://www.ibm.com/devops/method/tutorials/tutorial_toolchain_flow
[Conversation introduction]: https://www.ibm.com/watson/developercloud/doc/conversation/configure-workspace.html
[bluemix status]: https://status.eu-gb.bluemix.net/
[default coached conversation]: https://ibm.box.com/shared/static/02vrdvv3nt7uk7p23wnd6q09uzuwazo4.json
