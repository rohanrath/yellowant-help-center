Building Command Workflows



### Example:

In this post, we will explore command triggered workflows\(or “Crumbs” as we call it\) with an example. Let’s create one Slack command that gets a high-priority PagerDuty incident, creates a JIRA issue, sends an email to the Test team, and creates a calendar event for a war room meeting. Normally, this process would take atleast 5 minutes. With this command, it will take 5 seconds.

![](https://cdn-images-1.medium.com/max/1000/1*JwOI2pp_NuWyBrThxmzHBQ.png)

Let’s begin.

1. Create a [YellowAnt](https://www.yellowant.com) account. It’s free and takes 5 seconds if you have a Slack account. A @yellowant bot will be created inside your team Slack
2. Go to the YellowAnt marketplace. Search for and Integrate PagerDuty\([guide](https://blog.yellowant.com/acing-pagerduty-chatops-in-slack-with-yellowant-fa73b48639f8)\), JIRA\([guide](https://blog.yellowant.com/how-to-be-a-jira-ninja-with-slack-and-yellowant-58277dd31f0c)\), GMail\(easy\) and Google Calendar\(easy\).

![](https://cdn-images-1.medium.com/max/1000/1*P0iLLRJAhq2Hgzsh6Xtxyw.png)

* Click on “Integrate”

![](https://cdn-images-1.medium.com/max/1000/1*VDjqFESF49bNVkhtndJiMw.png)

![](https://cdn-images-1.medium.com/max/1000/1*9GymvKHXxUIDi6X2tPtakQ.png)

3. In the YellowAnt console, click on “Create a Crumb”. Crumbs are workflows

![](https://cdn-images-1.medium.com/max/1000/1*iaOEnh0lfUVcxzP8wTLocQ.png)

4. Click on **Create New**

![](https://cdn-images-1.medium.com/max/1000/1*D27svJzpWz6C6_U9GTt8JA.png)

Select **Command-based Crumb**

![](https://cdn-images-1.medium.com/max/750/1*U1jpqAETtDjOH0QVnr5t7Q.png)

In the Trigger area, select your custom command name. In this case, we have given _**war-room.**_ Our custom command will now start with **war-room**

![](https://cdn-images-1.medium.com/max/750/1*n-H1Q_KADHesi9NyJhnKEw.png)

In the **Input arguments** section, define the arguments\(or variables\) that this command will take. Click on **Add a new input argument.** In this case, the arguments will be **id**\(Id of the PagerDuty incident\).

It is now time to add some actions.

Our first action will be to search for the PagerDuty incident with Id **‘id**’. Our second action will be to create a JIRA ticket from the data that PagerDuty incident command returns.

Click on **Add Action.**

![](https://cdn-images-1.medium.com/max/1000/1*UwKCFpASlm2hsrNNGqLMMQ.png)

Select **PagerDuty**.

![](https://cdn-images-1.medium.com/max/1000/1*yY9FoYGb4NXUKDwkk_Ejhw.png)

Fetching incident details

In the actions, select **get\_incident**

![](https://cdn-images-1.medium.com/max/1000/1*Rnoiz46RsZGgamgsI_u2sA.png)

Fetching the incident details from PagerDuty

The get\_incident command takes one argument, i.e the **incident\_number.** This corresponds to the **id** that we will pass in the argument. Click on the **incident\_number** textbox and type **@ .**This will bring a dropdown of all the available variable that we will pass in our command. Select **id**.

The next action is to create a JIRA ticket. Click on **Add Action** and select **JIRA.** In the actions dropdown, select **createissue.**

The PagerDuty **get\_incident** command gives us a bunch of data to use to create a new JIRA ticket. Use the **@** symbol to select the variable in the inputs. You can use multiple variables within one input box — YellowAnt automatically concatenates them into one string.

![](https://cdn-images-1.medium.com/max/1000/1*b9YyRYB4vpRRLDqD7Ow25g.png)

Creating a JIRA ticket from Pagerduty data

It’s time to send a mail to the testing team

Click on **Add Action.** Select **GMail.** In the function list, select **send.**

![](https://cdn-images-1.medium.com/max/1000/1*osfade5aH7T6Xn1Olt0_tw.png)

Creating an Email from Pagerduty data

Format your **subject** and **message** using the **@** symbol to get data from the PagerDuty command.

It’s now time to call a war room meeting using Google Calendar.

Click on **Add Action.** Select **Google Calendar.** In the function list, select **create.**

Describe the event name — you can add some data from the previous steps using the **@** symbol. The **event** variable takes the event description in natural language. So you can say something like — **war room meeting for PD escalation @incident\_number in the next 5 minutes.**

![](https://cdn-images-1.medium.com/max/1000/1*f8k3ZrYVlIE3wOS2_5s4qA.png)

Creating a Google Calendar event

Click on **Save.**

