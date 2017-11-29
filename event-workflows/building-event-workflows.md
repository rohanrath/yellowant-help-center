# Building Event Workflows

In this section, we see step by step how to create an event workflow on YellowAnt. Following which, we will also cover a very common scenario as the example.

1. In your YellowAnt Dashboard, either from the Overview Panel or Event Workflows Panel, select "Add New" or "Create a Workflow" option respectively.  
   ![](/assets/ewf1.png)![](/assets/ewf2.png)

2. This will take you to the "Workflow Builder" page. Select "Create Event Workflow" from the two choices.  
   ![](/assets/select.png)

3. It automatically asks you for a "Trigger" application. The trigger application is the initiation application for the workflow. Here, we choose Pagerduty as the trigger application.  
   ![](/assets/ewf3.png)

4. Next step, asks you for a trigger event for the trigger application. That event is when the workflow starts. Here we choose an incident being assigned on Pagerduty as the trigger event.  
   ![](/assets/ewf4.jpg)

5. Choose a "Collection" in which you want to add the workflow to.

   Note: A collection is a way of segregating workflows into sets in order to keep them more organized for every individual. This is totally up to the user and can be treated as having different set of workflows where each set forms a collection with some specific set of tasks. Watch out for custom collections for different domains which will soon launch on YellowAnt.  
   ![](/assets/ewf5.jpg)

6. Click on "Add Action in the left panel.

7. Choose the application from which you want to use your first "Action". Here, we select "GMail".  
   ![](/assets/app1.jpg)

8. Choose the action you want to use from the application. Here, we select "Send an email".  
   ![](/assets/ewf6.jpg)

9. Fill in the required parameter field with the values you need. Here, we want a mail sent to the manager whenever a new Pagerduty incident is assigned. We can use values from the first step i.e. the trigger by using "@" in any of the text fields as shown. We can use it to compose mails in GMail or task names in Asana or use this information fields in different ways. The possibilities are endless.  
   ![](/assets/ewf7.jpg)

10. Click on "Add Action" in the left panel to add the second application.

11. Choose the application from which you want to use as your second "Action". Here, we select "Asana".  
    ![](/assets/app2.jpg)

12. Choose the action you want to use from the application. Here, we select "Create a task".  
    ![](/assets/ewf9.png)

13. Fill in the required parameter fields to create a task. You can use Pagerduty data to fill in details of the task.  
    ![](/assets/ewf10.jpg)

14. You can continue to create a chain of events across many apps. We will save it here. Click the button "Save" in the top panel.  
    ![](/assets/ewf12.png)

15. You will get a notification in your chat window about the creation of this new workflow.  
    ![](/assets/ewf13.png)

16. It will execute every time the initial trigger event occurs.



