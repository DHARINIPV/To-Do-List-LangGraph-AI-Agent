# To-Do List LangGraph AI Agent

This project demonstrates the construction and execution of a Task Manager AI Agent using LangGraph, an innovative framework for stateful, dynamic graph-based LLM applications.
The AI agent is built using LangChain’s ChatOpenAI and LangGraph’s StateGraph to facilitate a structured conversation loop that can ask for tasks and handle responses intelligently.

# Project Overview

## Objective:

Create a conversational AI agent that performs a looped workflow:

1. Ask the user for an action/task.

2. Process and store the response.

3. Loop back to ask again, enabling a simple form of task accumulation or dialogue flow.

## Frameworks & Tools Used:

LangGraph for graph-based AI execution logic.

LangChain for handling LLM calls.

OpenAI GPT-4 model via ChatOpenAI.

dotenv for managing API keys.

## How It Works

### 1. State Definition
The TaskState dictionary holds:

tasks: A list of completed or collected task responses.

message: The latest message exchanged in the dialogue.

### 2. Node Functions
ask_action(): Asks the user what task they’d like to perform.

handle_action(): Processes the user's response and appends it to the task list.

### 3. Graph Construction
Nodes and edges are defined using StateGraph(TaskState).

The graph runs in a loop (graph.add_edge("handle_action", "ask_action")) until manually stopped.

## Requirements
Python ≥ 3.8

openai, langchain, langgraph, dotenv

## Input and Output

<img width="517" height="698" alt="image" src="https://github.com/user-attachments/assets/5394b4df-8836-4d48-a5e6-df0eb26cf414" />

## Conclusion

This project is a stepping stone into the world of graph-based AI agents. By integrating LangChain’s conversational LLMs with LangGraph’s structured state machines, we’ve created an intelligent and extendable agent loop. It highlights how powerful LLMs can become when paired with robust execution flows.
Whether you're building smart assistants, automation tools, or dynamic bots—this architecture sets the stage for deeper, more controllable AI applications.
More importantly, it’s a fun, scalable way to turn language into logic.


