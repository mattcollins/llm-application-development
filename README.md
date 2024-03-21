# Best Practices for LLM Application Development

This is a guide to best practices for developing applications that make use of LLMs.

## AI Agents
As of March 2024, there are significant disadvantages to using agents. Only resort to them if you really need to.

### Disadvantages of AI Agents
* They tend to be less reliable than non-agentic calls.
* They're harder to test effectively as they can validly produce a wider range of outputs.

### Alternatives to AI Agents
Whatever task you're asking an agent to complete, can you break it down into a number of sub-tasks that can be orchestrated through some traditionally-coded logic?
