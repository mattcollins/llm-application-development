# Best Practices for LLM Application Development

This is a guide to best practices for developing applications that make use of LLMs.

## Have a Good Prompt Engineering Toolbox

### Provide Context
* Assign the AI a persona (e.g. "You are Steve Jobs")
* Describe a target audience (e.g. "You are writing for professional photographers")
* Specify an output format (e.g. "Create a 50-word summary")

### Give Examples (also known as 'few-shot' prompting)
Give examples of the sort of output you'd like.

### Use 'Chain-of-Thought'
Prompt the LLM to produce output that starts with some step-by-step thinking rather than generating an answer immediately.

### Use ['Panel-of-Experts'](https://sourcery.ai/blog/panel-of-experts/)
Ask the LLM to role-play a panel discussion.

## Use Multiple 'Passes'
If you're not getting the quality of results you want from a particular LLM call, consider breaking the task into several steps, each focused on a particular aspect of the job, and using an LLM call for each.

For example:
1. Create a draft
2. Edit the draft to ensure tone is correct
3. Edit the draft to ensure any quotes are accurate (original sources would need to be part of the context)

## Using AI Agents

### Avoid Agents if You Can
As of March 2024, there are significant disadvantages to using agents. Only resort to them if you really need to.

#### Disadvantages of AI Agents
* They tend to be less reliable than non-agentic calls.
* They're harder to test effectively as they can validly produce a wider range of outputs.

#### Alternatives to AI Agents
Whatever task you're asking an agent to complete, considering seeing if you can instead break it down into a number of sub-tasks that can be orchestrated through some traditionally-coded logic instead. This may be more reliable.

### Give AI Agents Very Limited Tasks
The more limited the scope of the task, the more likely the agent will be able to complete it.

## Have Good Evaluation Tooling
Read [Your AI Product Needs Evals](https://hamel.dev/blog/posts/evals/)

## Reducing Development Cycle Time

### Cache LLM Responses
Add a caching layer in front of LLM calls. This can make automated tests much faster (and reduce costs.)
