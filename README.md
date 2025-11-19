# Exno.7-Develop a prompt-based application tailored to their personal needs, fostering creativity and practical problem-solving skills while leveraging the capabilities of large language models.

# Date:
# Register no: 212223220107
# Aim: To develop a prompt-based application using ChatGPT - To demonstrate how to create a prompt-based application to organize daily tasks, showing the progression from simple to more advanced prompt designs and their corresponding outputs.

#AI Tools Required: 

* DeepSeek
* (Optional) ChatGPT / LLM interface
* Any text editor or command line

---

## ** Project Explanation**

This project showcases how prompt engineering can be used to build a **Personal Productivity Assistant** capable of:

* Managing daily tasks
* Scheduling events
* Giving wellness tips
* Answering general questions
* Adapting to user preferences

---

## ** Core Prompt Used**

```
Design a personal productivity assistant that can help manage daily tasks,
schedule reminders, suggest wellness tips, and answer general queries.
The assistant should interact using natural language and adapt to the user's
changing preferences over time.
```

---

# ** Contents**

1. Core Requirements & Simple Prompts
2. Intermediate Features (Contextual Prompts)
3. Advanced Features (Memory + Personalization)
4. Optional CLI Feedback Loop
5. Result / Outcomes

---

# **1️ Simple Prompt Examples**

## ** Daily Task Manager**

**Prompt**

```
Extract task, date, time, and priority from user input.
Return a JSON object.
```

**User Input**

```
Add "finish assignment" by tonight at 9 PM.
```

**Output**

```json
{
  "task": "Finish assignment",
  "time": "21:00",
  "date": "today",
  "priority": "high"
}
```

---

## ** Smart Scheduler**

**User Input**

```
Schedule a call with Riya at 4:30 PM.
```

**Output**

```
Conflict detected! You already have a 4–5 PM Code Review.
Try 5:30 PM instead?
```

---

## **Wellness Tips**

```
Tip: Try a 3-minute breathing exercise to refresh your focus.
```

---

# **2️ Intermediate Prompts – Contextual Understanding**

## ** Conflict Detection Example**

**User Input**

```
Add a language class at 11 AM.
```

**Existing Event**

```
11 AM – 12 PM: Doctor Appointment
```

**Output**

```
Warning: This overlaps with your doctor appointment.
Reschedule to 1 PM?
```

---

## ** Priority Sorting**

**Input Tasks**

```
- Pay electricity bill – High  
- Water plants – Low  
- Complete research notes – Medium  
```

**Output**

```
1. [High] Pay electricity bill
2. [Medium] Complete research notes
3. [Low] Water plants
```

---

# **3️ Advanced Prompts – Adaptive Memory & Personalization**

### **Simulated Memory**

```json
{
  "preferred_time": "evening",
  "disliked_tips": ["hydration reminders"]
}
```

---

## **Personalized Wellness Tip**

**Prompt**

```
Generate an evening wellness tip avoiding disliked suggestions.
```

**Output**

```
Try a 5-minute guided relaxation session tonight.
```

---

## ** Natural Conversation Interaction**

**User**

```
What am I supposed to do today?
```

**Output**

```
Your schedule today:
- 9:30 AM: Online seminar
- 1 PM: Prepare presentation slides
- 8 PM: Dinner with friends

Want to edit anything?
```

---

# **4️ Optional: CLI Simulation**

## **`cli_simulation.py`**

```python
while True:
    user = input("You: ")

    if "add" in user and "task" in user:
        print("Task added!")
    elif "tip" in user:
        print("Here’s a quick wellness suggestion...")
    elif "schedule" in user:
        print("Checking for conflicts...")
```

---

# **5️ Example Combined Output**

### **User**

```
Plan study revision and book a cab for 6 PM.
```

### **Assistant**

```json
{
  "tasks": [
    { "task": "Study revision", "time": "Flexible", "priority": "high" },
    { "task": "Book cab", "time": "18:00", "priority": "medium" }
  ],
  "summary": "Tasks added successfully. No clashes detected."
}
```

---

# Result: 
The lab exercise resulted in the creation of a prototype concept for a personal assistant powered by large language models. Students were able to:
 Understand how to tailor LLM prompts to real-life applications.
 Foster creativity by designing features suited to their personal or academic lives.
 Learn prompt engineering techniques for optimal interaction with AI tools.
 Experience the versatility and utility of generative AI in solving everyday problems.

---

