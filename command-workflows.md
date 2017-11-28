# Command Workflows

YellowAnt is connected to all your apps so you can create cross application workflows that can be triggered by a YellowAnt command. This means with a simple command you can trigger a chain of events across different apps and even use the subsequent data in the process. You can trigger a chain of events by executing a simple command on Slack or Microsoft Teams.  
Let's take a took at an example,

A lot of people, first thing in the morning, check their emails, tasks for the day on Asana/Trello, look at their schedule and maybe perform a bunch of other tasks as well \(like bugs due to be fixed or checking server statuses\). With YellowAnt, you can have a simple command like "startmyday" which fetches all this information in a nice and sequential manner for you.

![](/assets/startmyday.png)  
In this example, a simple command, "workflow startmyday" fetches mails from GMail and tasks due on Asana.

Take a look at another example.  
Let’s create one Slack command that gets a high-priority PagerDuty incident, creates a JIRA issue, sends an email to the Test team, and creates a calendar event for a war room meeting. Normally, this process would take atleast 5 minutes. With this command, it will take 5 seconds.  
![](/assets/warroom.png)  
Similarly, users can create lot of different commands for different purposes using 35+ applications from the YellowAnt Marketplace.

