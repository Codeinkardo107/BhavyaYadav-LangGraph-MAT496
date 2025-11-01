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
This notebook shows the use of checkpointer(one of the checkpointers - MemorySaver), which automatically saves the graph state after each step. Hence having memory, allowing langgraph to pick uo form the last state update and perform any set of functions.
- Added tools for getting the largest number and also for getting the remainder.
<br/>

---
---

<br/>

## Module 2
### 1) state-schema.ipynb
This notebook tells what is schema(it is just the structure and the types of data the gaph will use). How to define and use typed data structures (like TypedDict, Pydantic) to manage state, memory.
- Added an example of Pydantic which can perform validation to check whether data confirms to the specified types and contraints at runtime
<br/>

### 2) state-reducers.ipynb
This notebook demonstrates how reducers control state updates when multiple nodes modify the same key or run in parallel. How to define custom reducers to handle state merging safely(eg. None types). How to add messages, re-write messages, delete messages.
- Added an example in reducers, custom reducers
<br/>

### 3) multiple-schemas-ipynb
This notebook shows how to use multiple schemas - separate overall, secret, and input/output schemas so different nodes can handle specific data without exposing unnecessary state.
- Added an example of the input/output schemas
<br/>

### 4) trim-filter-messages.ipynb
This notebook shows how to trim and filter messages(based on any latest messages or depending on token used) with long-running conversation(high token usage), managing message history effectively.
Example of trimming messages depending on token used(set to 100).
- Added examples in reducer, trimming

<img width="1759" height="909" alt="image" src="https://github.com/user-attachments/assets/f20311a4-d395-4f8e-b940-31ac1914203e" />
<br/>
<br/>

### 5) chatbot-summarization.ipynb
This notebook shows how we go from simple conversation taking place across different invocations, to a continuosly updated internal summarization state that helps us having long running ocnversations with our assistant without a gread deal of token usage.
- Added a new varibale count(counts the total number of human-bot conversations as 1 and conversation with summary as 2)

<img width="1759" height="907" alt="image" src="https://github.com/user-attachments/assets/3031115f-4498-4108-a210-6be4308c2bce" />
<br/>
<br/>

### 6) chatbot-external-memory.ipynb
This notebook shows how to build a persistent chatbot using LangGraph with SQLite for long-term memory storage. The system automatically summarizes conversations when they get too long and maintains state externally.
- Shown new conversation in langgraph studio
- Added an example that counts the number of human messages in the conversation.

<img width="1759" height="867" alt="image" src="https://github.com/user-attachments/assets/28072a94-1a92-43df-9c72-1b0c00ec3018" />
<br/>
<br/>

---
---

<br/>

## Module 3
### 1) streaming-interruption.ipynb
This notebook demonstrates how to handle streaming interruptions - pause, resume, or restart graph executions during message streaming
- Added an example showing divison in streaming messages, another example in which shows the full state of a graph
  <br/>

### 2) breakpoints.ipynb
This notebook demonstrates how to use breakpoints to pause and inspect the state of a running graph by allowing manual intervention or state inspection before continuing.
- Added a new functon in tools to return whether the person is legal to drive a car or not, example added accordingly

<br/>
<img width="1759" height="868" alt="image" src="https://github.com/user-attachments/assets/e7ccef16-6d75-4aa8-a6f4-7c5ebf864b56" />
<br/>

### 3) edit-state-human-feeedback.ipynb
This notebook shows how to edit graph state using human feedback. It demonstrates how users can manually modify the graph’s state during execution to correct or improve results dynamically.
- Added a new function which calculates any(n1) percentage or any number(n2), example added accrodingly

<br/>
<img width="1759" height="868" alt="image" src="https://github.com/user-attachments/assets/1b3194cf-c1e6-483a-a9b8-b8da981a2265" />
<br/>

### 4) dynamic-breakpoints.ipynb
This notebook demonstrates how to use dynamic breakpoints, allowing pauses during execution. It shows how you can stop the graph at specific points based on runtime conditions for debugging or any kind of analysis. 
- Added a new interrupt condition for too long input (100 characters) and a corresponding example
<br/>

### 5) time-travel.ipynb
This notebook explores time travel, showing how to revert or replay a graph’s state from previous checkpoints. Demonstrates debugging, re-execution, and state restoration for better workflow control.
- Added a function for calculating the logarithm of number(a) to a base(b)
<br/>
<br/>

---
---

<br/>

## Module 4
### 1) parallelization.ipynb
This notebook demonstrates parallelization, showing how multiple nodes can run simultaneously to improve efficiency and reduce execution time in workflows.
- Added an example in waiting for node to finish, working with LLM
<img width="1759" height="868" alt="Screenshot 2025-10-31 183224" src="https://github.com/user-attachments/assets/64dca411-a531-4bf4-a32c-7b2bea5461c5" />
<br/>

### 2) sub-graph.ipynb
This notebook explains how to use sub-graphs in Langgaph, where smaller graphs are combined to from a larger one to create modular, reusable, and organized workflow structures.
In Langsmith you can view the sub-graphs or different components of the graph very easily(neately).
- Added an two sub graphs
<img width="1759" height="904" alt="image" src="https://github.com/user-attachments/assets/f9ac7ad1-4ef6-4fa7-97fd-ef48e98c1f12" />
<br/>

### 3) map-reduce.ipynb

<br/>

### 4) reesearch-assistant.ipynb

<br/>
