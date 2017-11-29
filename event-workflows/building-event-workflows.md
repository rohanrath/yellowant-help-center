# Building Event Workflows

In this section, we see step by step how to create an event workflow on YellowAnt. Following which, we will also cover a very common scenario as the example.

1. In your YellowAnt Dashboard, either from the Overview Panel or Event Workflows Panel, select "Add New" or "Create a Workflow" option respectively.   
   ![](/assets/ewf1.png)![](/assets/ewf2.png)

2. This will take you to the "Workflow Builder" page. Select "Create Event Workflow" from the two choices.  
   ![](/assets/select.png)

3. It automatically asks you for a "Trigger" application. The trigger application is the initiation application point for the workflow. Here, we choose Pagerduty as the trigger application.  
   ![](/assets/ewf3.png)

4. Next step, asks you for a trigger event for the trigger application, That event is when the workflow starts. Here we choose an incident being assigned on Pagerduty as the trigger event.  
   ![](/assets/ewf4.jpg)

5. Choose a "Collection" in which you want to add the workflow to.

   Note: A collection is a way of segregating workflows into sets in order to keep them more organized for every individual. This is totally up to the user and can be treated as having different set of workflows where each set forms a collection with some specific set of tasks. Watch out for custom collections for different domains which will soon launch on YellowAnt.  
   ![](/assets/ewf5.jpg)  

6. Click on "Add Action in the left panel.

7. Choose the application from which you want to use as your first "Action". Here, we select "GMail".  
   ![](/assets/app1.jpg)

8. Choose the action you want from to use from the application. Here, we select "fetch mails from a label".  
   ![](/assets/gmailaction.jpg)

9. Fill in the required parameter field with the values you need. Here, we want mails fetched with the label "UNREAD".  
   ![](/assets/fillreqdfield.jpg)

10. Click on "Add Action" in the left panel to add the second application.

11. Choose the application from which you want to use as your second "Action". Here, we select "Asana".  
    ![](/assets/app2.jpg)

12. Choose the action you want from to use from the application. Here, we select "List user tasks".  
    ![](/assets/asanaaction.jpg)

13. Fill in the required parameter field with the values you need. Here, we want tasks fetched from a workspace "yellowant.com".  
    ![](/assets/fillreqdfield2.jpg)

14. You can continue to create a chain of events across many apps. We will save it here. Click the button "Save" in the top panel.  
    ![](/assets/createdcw.jpg)

15. You will get a notification in your chat window about the creation of this new workflow. You can execute it right from there as well.  
    ![](/assets/check1.png)

16. To execute it at any point, just type "collectionname workflowname" and it executes. Example, "demo-collection startmyname".  
    ![](/assets/cmcmd.png)![](/assets/cwcmd2.png)

### Another Example \(more comprehensive\):



