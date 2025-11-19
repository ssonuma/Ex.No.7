Ex. No. 7 – Develop a Prompt-Based Application

Date: 

Register No.: 212223220107

Aim:

To develop a prompt-based application using ChatGPT — demonstrating how to design prompts to organize daily tasks, progressing from simple to advanced prompt structures and outputs.

AI Tools Required:

DeepSeek

Explanation:
Prompt Used:

"Design a personal productivity assistant that can help manage daily tasks, schedule reminders, suggest wellness tips, and answer general queries. The assistant should use natural language and adapt to the user’s evolving preferences."

Procedure:

Define the core requirements of a personal productivity assistant.

Draft and refine prompts for each feature (tasks, reminders, wellness tips).

Simulate user–assistant interaction using simple text-based workflows.

Collect feedback and modify responses accordingly.

(Optional) Add simulated memory to adapt to user preferences.

Expected Output:

(Based on example model response)

Personal Productivity Assistant – Features

Daily Task Manager

Accept tasks in natural language (e.g., “Add grocery shopping to my list.”)

Classify tasks by priority and deadline

Show daily summaries

Smart Scheduler

Set reminders or events

Detect overlapping tasks

Wellness Tips Generator

Provide daily wellness suggestions

Adjust advice based on user preferences

Conclusion

Below is the enhanced output section rewritten with different examples from the ones you provided earlier.

1. Core Requirements & Simple Prompts
Features:

Basic task creation, scheduling, wellness suggestions & question-answering.

Interaction:

User communicates in natural language, assistant responds with structured output.

a. Daily Task Manager

Prompt Example:
"Convert the user's sentence into structured task information. Extract: task, date, time, priority."

User Input:
“Add ‘finish assignment’ by tonight at 9 PM.”

Output:

{
  "task": "Finish assignment",
  "time": "21:00",
  "date": "today",
  "priority": "high"
}

b. Smart Scheduler

Prompt Example:
"Check whether the new event overlaps with existing events. Respond clearly."

Existing Events:

10:00–11:00: Team Briefing

4:00–5:00 PM: Code Review

User Input:
“Schedule a call with Riya at 4:30 PM.”

Output:

Conflict detected! Your 4:00–5:00 PM Code Review overlaps with this new call.
Would you like to schedule at 5:30 PM instead?

c. Wellness Tips Generator

Prompt Example:
“Suggest one wellness tip from: breathing exercises, mini-walks, posture correction.”

Output:

Tip: Try a simple 3-minute deep breathing exercise to reset your focus.

2. Intermediate: Contextual Understanding

Now the assistant can check conflicts, sort priorities, and consider preferences.

a. Conflict Detection Example

User Input:
“Add a language class at 11 AM.”

Existing Event:
11:00–12:00 Doctor Appointment

Output:

Warning: The requested 11 AM language class overlaps with your doctor appointment.
Would you prefer scheduling it at 1 PM?

b. Priority-Based Task Sorting

Task List Input:

Pay electricity bill – High

Water plants – Low

Complete research notes – Medium

Prompt Example:
"Sort by priority and return as list."

Output:

1. [High] Pay electricity bill  
2. [Medium] Complete research notes  
3. [Low] Water plants

3. Advanced: Adaptive Memory & Natural Interaction

Now the assistant simulates learning from past preferences.

a. Wellness Tips with Memory

Simulated Memory:
User dislikes long workout suggestions.

Prompt Example:
"Suggest a wellness tip but avoid workouts longer than 10 minutes."

Output:

Try a 2-minute shoulder relaxation stretch to reduce stiffness.

b. User Preference Adaptation

Simulated Preference JSON:

{
  "preferred_time": "evening",
  "disliked_tips": ["hydration reminders"]
}


Prompt Example:
"Generate an evening wellness suggestion."

Output:

Wind down with a 5-minute guided relaxation session this evening.

c. Natural Language Interaction

User Input:
“What am I supposed to do today?”

Task Data:

9:30 AM: Online seminar

1:00 PM: Prepare slides

8:00 PM: Dinner with friends

Output:

Here’s your plan for today:
- 9:30 AM: Online seminar  
- 1:00 PM: Prepare your slides  
- 8:00 PM: Dinner with your friends  
Let me know if you want to make changes!

4. Optional: Feedback Loop & Interface Simulation
Feedback Example:

Assistant: “Was this suggestion helpful?”
User: “No.”
Assistant: “Thanks! I’ll avoid similar tips next time.”

Command-Line Simulation (Example Logic)
while True:
    user = input("You: ")

    if "add" in user and "task" in user:
        # Process task manager prompt
        print("Task added!")
    elif "tip" in user:
        # Provide adaptive wellness tip
        print("Here’s a quick wellness suggestion...")

Expected Output Example (Different Example)

User:
“Plan study revision and book a cab for 6 PM.”

Assistant:

{
  "tasks": [
    { "task": "Study revision", "time": "Flexible", "priority": "high" },
    { "task": "Book cab", "time": "18:00", "priority": "medium" }
  ],
  "summary": "Both tasks added successfully. No schedule clashes found."
}


User:
“Give me a wellness tip.”

Assistant:

Since you prefer short activities: Try a 1-minute eye relaxation exercise!

Result:

The experiment successfully produced a functional prototype of a prompt-based personal assistant using LLMs. Students:
✔ Understood how to convert real-life needs into LLM prompts
✔ Practiced creativity while designing assistant features
✔ Learned prompt-engineering concepts for efficient AI interactions
✔ Explored practical use of generative AI for everyday productivity
