# Alorithm Logic for Emento-Task prototype

This is the algorithm logic for Claude to follow for the Emento-Tasks project.  
  
Claude should build the relevant scripts to use in the prototype, following this logic.  
  
**Goal of the project**
- Build a functional prototype to showcase an idea
- The idea is to create personalised task list based on patient characteristics and the number of days until an appointment
- For example: a low health-literacy patient with only two days until a surgery would see more simple messages and more daily tasks 
- For example: a high health-literacy patient with ten days until a surgery (and who smokes) would see fewer daily tasks and key smoking information

## Algorithm Overview
- The input will be 1) patient characteristics, captured in the form in the ‘Start’ screen, and 2) the table at the end of this file
- The output of this algorithm is to make the tasks that will be displayed in the prototype on the ‘Task’ screen.
- The outputs should be:
	- 1) Title of task (to be shown in the screen)
	- 2) Day tags for the task (day 1, day 2, day 3…to inform what day of the patient’s journey a task is for). And order of tasks within a group (1.1, 1.2, 1.3, etc.)
	- 3) Tags for if the task is a notification

**How the information should be used:**
- Claude should build both the algorithm and the integration with the prototype, so that:
	- A tester fills out the form
	- The tasks are personalised in both content and order (following the guidance below)
	- The personalised tasks are then displayed in the ‘Task’ screen with correct titles, order, and, if relevant, a notification icon
	- The tags are used when the Tester presses the filter buttons. 
		- “Alle”: show all tasks
		- “I dag”: for this prototype, let’s assume it’s Day 1
		- “Overskredet”: for this prototype let’s assume that only the first task is ever completed, the remaining are incomplete

## Algorithm Logic

Take the input about the patient and their operation and use the below table to create the titles of the tasks and the relevant tags for order, grouping, and notification icon.  
  
**Key Guidance:**
- Create as many ‘pre days’ as fits before the operation
- Separate sections into the days as makes sense, always keep sections together
	- For example: if there are three days before the operation, then there should be three days before the operation appointment card in the task list. Put all the tasks from Sections A&B into ‘Day 1’, all the tasks from Sections C&D into ‘Day 2’, and then all the tasks from Section ‘E&F’ into ‘Day 3’.
- Only Include Section D if the patient is a smoker
- Exclude any tasks for a High Health Literacy patient (HHL) if the table says exclude - this is additional info they don’t need
- Use a HHL or LHL title depending on if the patient has High Health Literacy or Low Health Literacy
- For any tasks that have specific timing, give them a notification icon tag, and make sure they appear in the right position in the task list 
	- For example: the Fasting Before 6 hours should appear 6 hours before the start of an operation  
		  

| Section | Pre-Op | Non-Smoker | HHL     | Title: HHL                              | Title:LHL             | Notification | Timing               |
| ------- | ------ | ---------- | ------- | --------------------------------------- | --------------------- | ------------ | -------------------- |
| A       | Yes    |            |         | Welome                                  | Hello                 |              |                      |
| A       | Yes    |            | Exclude |                                         | Good tips             |              |                      |
| B       | Yes    |            |         | About the Operation                     | What will happen?     |              |                      |
| B       | Yes    |            |         | Anesthesia                              | You will be out       |              |                      |
| C       | Yes    |            |         | Get ready                               | Get ready             |              |                      |
| D       | Yes    | Include    |         | Smoking is bad                          | Smoking is bad        |              |                      |
| E       | Yes    |            |         | Helpful information about operation day | Good tips again       |              |                      |
| F       | Yes    |            |         | Start Fasting!                          | Start Fasting!        | Yes          | Day Before Operation |
| G       | No     |            | Exclude |                                         | After operation       |              |                      |
| H       | No     |            |         | Take care of your leg                   | Take care of your leg |              |                      |

