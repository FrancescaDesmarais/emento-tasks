# Emento Tasks: Research Background

This is helpful background content for Claude for the Emento-Task project.

### Starting Point
The Emento App is a patient-support app for people being admitted to hospital. For example, Francesca used it for a knee surgery. A nurse ‘creates’ a new journey for a patient and then they get information specific to their operation or procedure. It should help patients better prepare and care for themselves before and after a hospital admission, while saving nurses time.  

### The Challenge
The main screen of the app has a list of ‘tasks’ that a patient can go through to prepare for the operation and recover after the operation. In Francesca’s experience of using the app, she noticed a number of small opportunities to make it better:
- The biggest reflection was that the task list seemed generic - like it was made for any patient, not Francesca specifically. For example, Francesca had task items that were from weeks before her journey had been created: the dates didn’t make sense. Or there was information about if Francesca used a walker, but she doesn’t so that information wasn’t helpful.
- Francesca also found that there was no hierarchy to the task list. She mentally bucketed tasks into things _before_ and _after_ the operation, but all of the tasks looked the same. A long flow of similar looking tasks.
- Some tasks are information based, some are more notification based.
- And lastly, Francesca found the content architecture a bit random. Repetition can be really helpful, but why did she need to know the WiFi password in the first welcome message (this would have been far more helpful closer to the operation day). Or why was a note to book transport in the ‘Getting Ready’ task, but a link to book transport in the ‘Info’ tab totally outside of the task list? And why was information about alcohol and smoking in the ‘Info’ tab?

Francesca had some other reflections from her knowledge of patients accessing healthcare:
- Francesca got the impression that the text is the same for any user, but she knows there’s a wide spread of health literacy. It could be very cool to adjust the actual copy (i.e. the message) and the order of tasks depending on the health literacy of a patient.
- Elderly people consume healthcare at far higher proportions than the rest of the population, yet the app didn’t have responsive text sizes. Francesca couldn’t zoom in to read anything more clearly. And sometimes there was a lot of white space (for example: a user clicks on a task, it has three sub-tasks, the user clicks on a sub-task, it only contains a short sentence of text…the rest of the screen is just white space…and the user can’t zoom in)

### The Opportunity
Rather than provide a generic list of tasks \> personalise the task list based on a few key characteristics of a user. The solution should:

1) personalise the order and message content based on a patient’s health literacy, and 
2) break up the pre-operation tasks into daily ‘chunks’ that make sense.
- For example, if there are ten day before the operation, make ten chunks. But if there are only 2 days before the operation make two chunks.
