# Actions for Event Workflows

An Action is a task that is performed after the trigger event occurs. For any event workflow to work, there has to be at least one action too. This is a very simple relationship - the trigger event acts as the stimulus for the next step i.e. the action. 

Example: ![](/assets/stim.png)In this case, the trigger is a Jenkins job notification and the action is sending an email in GMail. 

Now actions can occur based on conditions also, which we will cover in the next part of the documentation.

