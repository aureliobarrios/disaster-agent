# disaster-agent
A disaster news agent with connection to Slack that updates a user on disasters news around their area. This agent was built using the n8n workflow.

This agent leveraged API connections to Slack, Google News, Geolocation to build disaster news knowledge of a users area. This agent also leveraged a Postgres database to handle all user interactions and save chat history.

## Workflow

The agent followed the following workflow.

1. Receive user input from Slack using Slack API
2. Pass through initial Disaster Agent that Geolocated the user and used this information to gather disaster news around the users area
3. Pass through second Local News Agent that summarized disaster news and added additional context (local news) to user output
4. Return response to Slack using Slack API

![](/images/disaster-agent.png)

## Agent Response

An example of the agents response

![](/images/agent-response.png)