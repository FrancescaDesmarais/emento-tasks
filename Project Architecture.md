# Project Architecture

This is the project architecture for Claude to follow for the Emento-Tasks project.  
  
**Goal of the project**
- Build a functional prototype to showcase an idea
- The idea is to create personalised task list based on patient characteristics and the number of days until an appointment
- For example: a low health-literacy patient with only two days until a surgery would see more simple messages and more daily tasks 
- For example: a high health-literacy patient with ten days until a surgery (and who smokes) would see fewer daily tasks and key smoking information

**Who will use this prototype?**
- This prototype will be used by people, we will call them ‘testers’
- They will test the prototype, click through and use it’s functions to understand the goal and key concept behind the solution that is being prototyped
- Testers have a deep understanding of the app, this prototype is to communicate internal ideas

**Prototype Language**
- The prototype should be in Danish
- Francesca will try her best to make all copy in Danish, but Claude should translate any remaining English copy into Danish

## Page 1: Start Page
- The goal is to inform the tester what feature they are testing and set the patient characteristics
- In this case: a personalised task list based on a patient and their situation
- There should be centered text that says: “Set Key Patient Details”
- And then below the text, a form to input information (see below for form details)
- The form should have tight padding, not too much space, easy to quickly fill out. It should fit a container the width of the above text, and be left-aligned.
- The background color should be a gray - this is a bit of a ‘back-end’ page that any real patient would never see
- Below the form is a button that says “Personalise Task List”

**Patient Characteristics Form**
- Days to operation: (enter number)
- Patient’s health literacy: (high-low toggle)
- Patient is a smoker: (check box)

**Key Action:**
- Testers fill out the form and then press a button that says “Personalise Task List”

## Task List
- This is the main screen of the prototype
- It should look like a wireframe of the existing Emento App. Base the structure off of this screenshot: ![][image-1]
- It should have a title bar with a title and a back button, and filter buttons below the title
	- Title: “Knæoperation - menisk”
	- 3 filter buttons: “Alle” / “I dag” / “Overskredet” 
	- Note: REMOVE the search function, no search icon for this prototype
- Below the title bar are the tasks
	- As you can see in the screen shot, the tasks are rectangular cards with text and then either a check mark or a red circle (completed, not completed)
	- Follow the Algorithm Logic (in the Algorithm mark down file) to create the personalised list of tasks for the screen
	- Instead of using dates, follow the Algorithm Logic (in the Algorithm mark down file) to populate and group tasks into day chunks. Use horizontal lines to separate each group of tasks, and give each group a title:
		- For example, ‘Day 1’ for the first day of tasks, ‘Day 2’ for the second day of tasks, etc.
		- There should be as many days before the surgery as was input in the starter page.
	- If a task is a notification, use a simple notification icon to indicate that the task has a specific time or date requirement
	- Their should be a specific card for the operation day, that looks different than the other tasks. This is the anchor that clearly indicates what tasks comes before and after the operation.
		- Make the operation apointment card look like the appointment card in this screenshot from the Emento App (large date, vertical line, apt info): ![][image-2]
	- The tasks are scrollable
- Anchored at the bottom of the screen is the tab bar with icons for the Emento app screens. Make a wireframe version that copies exactly the order, icons, and text of the existing app tabs for the screens. Highlight ‘Tasks’ with the feature color since this is the active screen.

**Color of Task List Screen**
- Use black and white and gray tints as much as possible, except for the below cases
- Any active buttons should be the feature color, inactive buttons should be a tint of the feature color (so that it’s clear they are part of the prototype and can be clicked)
- The active ‘Tasks’ in the tab bar should be the feature color (all others a darker, inactive gray)
- The operation day card should have a border in the feature color, and have a tint of the feature color as background color.
- Behind the tasks is a gradient that extends from full white to the background tint of the operation day card. It should build towards the tint as the tasks get closer to the operation day, and then fade away from the operation card as the tasks get further out. The effect is to show momentum and visually distinguish the patient’s journey towards and then away from the operation.

**Key Actions**
- Testers can press the back button in the title bar and return to the start screen
	- They should be prompted with a pop-up screen that says “Restart the Prototype? With a yes or no button” (yes leads to the start, no returns to task screen)
- Testers can scroll the tasks list
- Testers can press on the filter buttons to filter the tasks
- Testers can press on the operation appointment card to open it’s details
	- Base that screen off this screenshot from the app: ![][image-3]


[image-1]:	file:///Users/francescadesmarais/Documents/Claude%20Projects/emento-tasks/images/IMG_0609.jpg
[image-2]:	file:///Users/francescadesmarais/Documents/Claude%20Projects/emento-tasks/images/IMG_0608.jpg
[image-3]:	file:///Users/francescadesmarais/Documents/Claude%20Projects/emento-tasks/images/IMG_0610.jpg