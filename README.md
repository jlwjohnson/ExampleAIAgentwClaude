# Example MCP Remote Client connector within AI Orchestrated workflow
Tutorial files for a simple MCP and Camunda AI agent
* Make a Request (form)
* Get More Information (form)
* Display Results (form)
* Review AI Resutls (form)
* AI Agent Chat with MCP and Claude Agent (BPMN)
* MCP Remote Client Connector A (connector template)

## The AI Agent
The AI Agent calls 4 possible tools:
* DeepWiki to get information about a github repository. 
  NOTE: You *must* be sure to use a repository already indexed for DeepWiki. Some suggestions are:
   * github.com/tensorflow/tensorflow
   * github.com/facebook/react
   * github.com/pytorch/pytorch
   * github.com/kubernetes/kubernetes
* A Claude SDK Joke API (via REST)
  The options for jokes are of type:
  * animal
  * dad
  * kid
* A product calcluation
  This merely takes some numbers and performs a calculation on them and provides the produdct back.
* Get more information
  This is a human task to request more information, if needed.

## Review AI Performance 
When displaying the AI Agent results, there is a Yes/No section to review the AI Performance. If "Yes" is selected, an AI Agent will run to evaluate how well it believes it responded to the request and then will provide that information in the form step following that follows this agent.

## Suggested Requests
Some suggested requests are:
* "Can you do a product calculation for 2 and 7 and then give me a good dad joke?"
* "Can you provide information github.com/tensorflow/tensorflow?"
* "Can you provide a product calculation for 3 and 8 and information on github.com/pytorch/pytorch?"
* "Can you do a product calculation for two numbers and then provide a animal joke?"