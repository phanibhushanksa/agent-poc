# What is an AI Agent?

#### *Is it a secret agent like James bond?Lol no, but the AI agents are equally or more capable than a secret agent.*

* Agent is an AI Model capable of reasoning, planning and interacting with its environment.  (It uses external tools to get things done)
* We call it Agent because it has agency, aka it has the ability to interact with the environment.

* An Agent is a system that leverages an AI model to interact with its environment in order to achieve a user-defined objective. It combines reasoning, planning, and the execution of actions (often via external tools) to fulfill tasks.

![alt text](assets/agent_process.jpg)

Agent has two main parts
#### 1. The Brain (AI Model):
    * The AI model is capable of thinking and taking decisions by itself. It handles the reasoning and plans which actions to take based on the situation. 
    * We can use LLM which take text as input and VLM (Vision Language Models) also which take images as input. 
#### 2. The Body (Tools):
    The external tools that are equipped to the system. For example - ## TODO (weather API maybe)


#### How does an AI interact with it's environment?
* LLMS are only capable of generating text. But can use external tools to perform more complex tasks. For example, ChatGPT uses image generation tool to generate images, when asked in a prompt. 

#### What type of tasks can an Agent do?
* An Agent can complete any task via *Tools* to complete *Actions*

For example: We can ask an Agent "Will it rain today in Tampa?". For that we need to provide a Tool, which can be written in Python as:
```Python
def get_weather(lat:str,lon:str):
    """Return the weather based on the location given"""
    WEATHER_API = "XXXXXX"
    weather = request.get(lat,lon)
    return weather
```

The brain of the Agent, i.e. the LLM will generate code to run the tool when it needs to, and fulfill te desired task.
```Python
get_weather(lat="160.7",lon="132.89")
```

### Design of Tools

* Design of the Tools is very important and has a great impact on the quality of your Agent. Some tasks will require very specific Tools to be crafted, while others may be solved with general purpose tools like “web_search”.

#### Note: 
* *Actions* are not the same as *Tools*. An Action can involve the use of multiple Tools to complete. 
* Actions are the steps the Agent takes, while Tools are external resources the Agent can use to perform those actions.

### Examples

1. Virtual Assistants like Google Assistant, Siri etc
They work as agents when they interact with other apps based on a user query. They take a user query, analyze context, retrieve information from databases, initiate actions like setting a reminder, responding to a text, provide responses etc. 

2. Customer Service Chatbots
Many companies deploy chatbots as agents that interact with customers in natural language.
These agents can answer questions, guide users through troubleshooting steps, open issues in internal databases, or even complete transactions.

### To summarize, an Agent is a system that uses an AI Model (typically an LLM) as its core reasoning engine, to:

* Understand natural language: Interpret and respond to human instructions in a meaningful way.
* Reason and plan: Analyze information, make decisions, and devise strategies to solve problems. 
* Interact with its environment: Gather information, take Actions using Tools, and observe the results of those actions