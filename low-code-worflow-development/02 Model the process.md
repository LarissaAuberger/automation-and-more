# Create the process application
A process application is a container that stores process models and supporting implementations. A process application typically 
includes processes, the services that implement activities and integrate with other systems, 
and other items required to run the processes. 

You create the process application to contain the Standard HR Open New Position process.

1. Navigate to the provided URL on IBM Cloud.
2. Select the authentication type `Enterprise LDAP` and login with the provided user
![Login](graphics/pic01.png)
3. Find the card `Recent Business Automations` and click `Get started` if no artifacts exist yet. Otherwise, click `View all`

![Get started](graphics/pic02.png)
4. In the `Business automations` view click `Create` and select `Workflow` -> `Workflow automation`
![Get started](graphics/pic03.png)
5. To be able to differentiate your process application from those of other lab participants, provide a unique name for your 
process application, e.g. `User1 Hiring Sample`. Add a description, e.g. `Contains the process for filling a position.`
![Create a workflow application](graphics/pic04.png)
6. Click the blue `Create` button.
7. The business automations authoring environment opens editing the process application you just created.


# Create the process
In this section you will create a process, a reusable process diagram that defines what is common to all runtime instances of that process model.
1. Make sure your process application is open in the authoring tool.
2. In the library, click the plus sign next to `Processes` and select `Process`.
![Process](graphics/pic05.png)
3. Provide a name for the process, e.g. `Standard HR Open New Position` and click Finish.
4. The process is created and the process diagram opens showing the following modeling constructs
![Modeling](graphics/pic06.png)


The initial interface of the authoring tool includes 
  - Library (1) - provides access to the library items for the current process application.
  - Main canvas (2) – The area in which you can graphically model your process and the other artifacts that you create in the process application. 
  Each process automatically includes a start event and an end event. Two default lanes are included for team and system tasks.
  - Palette (3) – Provides elements that you can use to model your process.
  - Properties (4) – Provides the properties of any element that you select in the main canvas.
5. Open the `Overview` page and add a description.

![Overview](graphics/pic07.png)
6. In the `Exposing` section click `Select` for `Expose to start` and then select `All Users`. This means that all users in the system will be allowed to
start an instance of this process.

![Exposing](graphics/pic08.png)
7. Save your changes.

# Add activities and events
In this section, you add activities and events to the lanes in the Standard HR Open New Position process to establish the correct process flow.

When you add activities and events, follow these guidelines:

- Ensure that activities represent logical units of work that are assigned to a participant of a process.
- Create multiple concurrent workflow steps that are assigned to one responsible role into one activity or task.
- Use verb-noun statements to label activities, such as “Submit position request”.
- Apply a top-down, left-to-right flow to your process so that it is easier to read.

Be aware of the following concepts:

| Concept | Description |
| ----------- | ----------- |
| Event | Controls flow objects for a process model. An event is something that occurs during a process. |
| Start event | Triggers the initiation of the process through a manual or automatic input. There are four types of start events - none, message, ECM content, and document. In a process, a none start event is created automatically and only one instance is allowed in the model. To start a process when an external signal is received, add a message start event to the process. |
| End event | Occurs in a process when a final decision from all activities or a partial set of activities is reached. There are four types of end events: none, message, error, and terminate. You can have multiple standard end events. |
| Activity | A single work task that a participant, whether the participant is a person or a system, accomplishes from beginning to end during a process. There are many types of activities: For example, user task, system task, script, and decision task. |
| User task | An activity is implemented as a user task when a user or human starts or completes the activity. For example, the `Submit position request` activity is a user task. |
| System task | An activity is implemented as a system task when an automated system or service completes an activity. For example, the Notify hiring manager activity is a system task. |
| Script task | An activity that uses JavaScript to access and manipulate data. |
| Decision task | An activity with a decision or condition in a business rule to determine which process implementation is started. |

Model the process:
1. Go back to the Definition tab of your process.
2. The Inline User Task is created by default when a process is created. Select this task and delete it. Also delete the arrow between the Start and the End event.
![Inline User Task](graphics/pic09.png)
3. Click the Team lane and, in the Properties tab, change the name to Hiring Manager. As Color, select green.
![Hiring Manager Lane](graphics/pic10.png)
4. Drag and drop a User Task activity from the palette into the Hiring Manager lane. 
![User Task](graphics/pic11.png)
5. Click the activity and type Submit position request.
6. In the Properties under the Documentation tab change the color of the activity to Blue and add a description for the activity.
![User Task](graphics/pic12.png)
7. Add the remaining Lanes and activites using the information in the following table
![Tasks](graphics/pic13.png)

Note: You will find the Lane element in the palette (the most top element). To add a new Lane to your process model, drag and drop this element.

8. Select the Notify hiring manager activity and then in the properties for the activity type, select Script.
9. Move the End event to the right of the Notify hiring manager activity. Your diagram matches the following image:
![Tasks](graphics/pic14.png)

Note: your work is continuously saved. You can also manually save your work when finished editing.
![Tasks](graphics/pic15.png)

# Model teams

# Add sequence flows

# Add event gateways

# Add a timer intermediate event

# Create process variables


# Conduct playback zero

