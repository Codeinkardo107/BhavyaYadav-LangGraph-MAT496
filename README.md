# Langgraph Poject
SUMMARY

By: Bhavya Yadav, 2410110101

---
---

## Module 1
### 1) simple-graph.ipynb
This notebooks shows the core components of langgraph. It’s a simple demo showing how LangGraph can create and run a branching workflow (“decision tree”) that randomly picks between two possible outcomes — happy or sad — and builds a corresponding sentence.
- Added an example with a decision tree corresponding which number to add - 1 or 2

<br/>
<img width="1759" height="866" alt="image" src="https://github.com/user-attachments/assets/396f5c9d-a546-43ff-934e-792ee89407d2" />
<br/>
<br/>

### 2) chain.ipynb
This notebook includes usage of chat messages in graph. Using chat models, binding tools to our LLM and executing those tool calls in the graph.
- Added extra tools for calculating division and power of some given numbers (a and b)
<br/>

### 3) route.ipynb
This notebook demonstrates the LLM directing the control flow either by calling a tool or just repsonding directly.
- Added a prime tool for calculating if the given number is prime or not. (Did not add the prime tool in the studio/router.py file)
<br/>
<img width="1759" height="866" alt="image" src="https://github.com/user-attachments/assets/309e46a7-0c5e-4fb8-a7bb-601dc3389853" />
<br/>
<br/>

### 4) agent.ipynb
This notebook inlcudes generic agent architecture. Invoke the model, if it chooses to call a tool, the returned ToolMessage is then given back to the model and let the model decide, whether to call another tool or or just respond directly.
- Added an example with tools(prime, power) and invoking the model.
<br/>
<img width="1759" height="906" alt="image" src="https://github.com/user-attachments/assets/15249c89-0640-4919-8bd3-c27a17b71ac1" />
<br/>
<br/>

### 5) agent-memory.ipynb


<br/>

### 6) deployment.ipynb

<br/>

---
---

<br/>
