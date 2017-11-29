# Using Action Outputs

One important feature while creating workflows is to use action outputs. Action outputs are the outputs of a previously added action or coming right from the trigger event itself. You can access the action outputs by using "@" in any text field in the subsequent actions.

Example:

In the trigger "incident assignment in Pagerduty", a whole lot of data is sent along with the event for us to use in the subsequent actions.![](/assets/trego1.png)

In this step, we see action outputs from Pagerduty being used to create an email body for GMail. At the same time, we can a whole lot of action outputs coming from GMail's send function as well.![](/assets/treg2.png)

In this step, we have action outs of both GMail and Pagerduty available to us for use. Also, we can see "create a task" on Asana is generating more action outputs that you can use.![](/assets/treg4.png)

