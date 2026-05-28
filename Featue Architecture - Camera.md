# Feature Architecture - Camera

This is the feature architecture for Claude to follow for the Camera flow for the memento-tasks project.  
  
**Goal of the feature**
- Build a functional prototype to showcase an idea
- The idea is to translate paper notes into relevant content that can be added into the Emento App
- For example: a piece of paper with pain management information could be captured and the information put into the patient’s task list

**Who will use this prototype?**
- This prototype will be used by people, we will call them ‘testers’
- They will test the prototype, click through and use it’s functions to understand the goal and key concept behind the solution that is being prototyped
- Testers have a deep understanding of the app, this is to communicate internal ideas

## Start Icon
- The goal is to highlight a new possibility: Camera!
- In this case: a camera input option to take a note from a nurse and input the relevant information into the Emento App
- In the right, upper hand corner of the view with task lists should be an icon of a camera with a “+” symbol. The icon should be blocky, and also fit the sketch visual style of the entire project.
- When a tester clicks on the icon, a pop-up should appear that tells the tester what they are about to do. Text: “Add Information To Your Digital Care Guide”

**Key Action:**
- Testers can click the camera+ icon to navigate to the camera function
- Pop-up to navigate forward ‘Yes’ to camera or ‘Back’ to the task list

## Camera
- Should open the native camera app on the phone
- Allow testers to take a photo

**Key Action:**
- Take a photo using the native camera app

## Analyse Image
Claude will mock up a potential use case for the tester to see:
- Have an analysing screen where the system is reading the image, let the tester know that something is happening
- Show the analysed information: In this case, a pain medication schedule. Show the image, show the key information, and give the tester the option to ‘Add to Care Journey’

| Mock Outcomes                      | Image                                          | Text from Image                                                                                                                                                                 |
| ---------------------------------- | ---------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Option B: Pain Medication Schedule | ![Example Image to Use for Prototype][image-1] | Paracetamol - Start 23/03 - Slut 27/03 2 tablet (2x500mg) Morgen, Middag, Aften, Nat  Tramadol - Start 23/12 - Slut 25/12 - 1 tablet (1x50mg) efter behov - Højst 4 gang daglig |

**Key Actions:**
- There should be a ‘back button’ in the upper left-hand corner so the tester can go back to the “Start Screen”\*\* - There should be a “Add to Care Journey” button at the bottom

## Show Updated Care Journey
After a tester clicks on the ‘Add to Care Journey’ button they should visually see an animation of how the information is added in. Let’s overdo the animation so that it is very clearly communicated: 
- The tester is shown the task list screen
- NOTE: If the tester has previously tried the camera feature, they should be shown a clean task list view (i.e. without any pain medication cards). So the testers always ‘restart’ this view of the prototype.
- New tasks are animated into the task list. A ‘Remember paracetamol’ notification card appears three times a day for the four days after the operation day. The previous cards visually move up/down so that there’s place for the new cards to fade into the new space. Maintain the background fade positions, just move the cards.
- The new task cards should look like the other notification cards with an alert icon
- The cards should load in with the action highlight color (pink) and then, once fully loaded, fade back to the color of task cards
- The card ‘I: How to manage your pain’ should also highlight pink and then fade in the same time as the new task cards, indicating that the information was also captured in this task.

**Key Actions:**
- The tester is back on the Task List screen, so they should have the existing options to go back and restart the whole prototype, or click on the camera icon and restart the camera flow.

[image-1]:	file:///Users/francescadesmarais/Downloads/IMG_0547.jpg