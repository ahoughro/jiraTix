Adventures in Data Mining Jira Tickets and working with AWS Comprehend

It all started one sunny afternoon on a work phone call during our creation of a Cloud Center of Excellence (CCOE).
How do we help our cloud users get easy answers to common questions?  We can create FAQ's, but, wait, What questions do our customers want answered?

We have thousands of Jira tickets that document what our cloud users have been asking since 2021, it should be really easy to send that information to a natural language processing tool and it will concisely tell me the topics that were most requested, right?

Not so much.  

This is not something I can drop into ChatGPT due to proprietary information that should not be shared outside the confines of work.

This is not a simple plug in text and get results into AWS Comprehend, much to my dismay.  

Here begins my journey with understanding how to use AWS Comprehend and gaining insights from Jira Tickets.

First, you can query your jira system using the Jira REST API (https://developer.atlassian.com/cloud/jira/platform/rest/v3/intro/)

As a newbie working with API calls, I was lucky enough to have some guidance on creating my initial query which can be put into a web browser like this:
https://jira.<YOUR_COMPANY>.com/jira/rest/api/2/search?jql=project=<YOUR_PROJECT>AND............
Components if you have them and 
Fields if you know which Jira fields you'd prefer to pull out.  In my case, our tickets include a unique key, summary, date created, and description.


