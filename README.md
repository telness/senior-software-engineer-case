# senior-software-engineer-case

## Overview
Hello there! Thanks again for your interest in joining our development team and congrats on moving forward in our recruitment process.

We employ case studies to assess candidates' practical thinking and decision-making abilities in real-life scenarios. This allows us to gauge your problem-solving skills, analytical approach, speed in generating solutions and workflows, logical reasoning, effective communication, and presentation style, as well as gain insight into how you would perform in this role if you were to join our team.

## Building and scaling Telness Tech's mobile and PBX service for the future

### Context
You are tasked with creating a system to handle all calls, both mobile and PBX, for Telness Tech. The service will be receiving requests when a call is initiated and must respond within a short time frame about what to do. If a response isn’t sent within a timely manner the call won’t go through.

Since the service controls calls if it is down or responding too slowly, the calls won’t go through.

### Background
- The service must respond within 3s per request, slower than that is treated as no response at all.
- The service will receive an HTTP POST request with a payload that contains information about the call, the response must contain a payload with information about what to do next.
- For mobile calls, the service only needs to do an initial response, and then the call is handled between the mobile phones themselves.
- For PBX calls the service will be continuously receiving requests as the PBX can consist of multiple parts with varying complexity (e.g., queues, menus, prompts etc).
- The service will need to communicate with other services to be able to determine what to do with calls.

### Technology
- The service will be deployed to AWS using EKS.
- The service will be written in Golang and will have a Postgres database.
    - This matches what all other services at Telness Tech use.
- If you deem it necessary, motivate why some other choice of technology would be preferable.

### Restrictions
- The service should be able to handle hundreds of thousands of mobile users.
- The service should be able to easily be deployed to new countries, keeping the same performance.
- The service should be cost-efficient, both for smaller (thousands of users) and larger customers (hundreds of thousands of users).
- Uptime is everything, customers can have extremely critical PBXes (e.g., ambulance service) where even a few minutes of downtime can mean literal life or death.
- It’s a startup, we don’t have infinite resources and we need to get something out quickly that we can iterate on.

### Task
You are the project lead and it’s your job to come up with an architecture for the service that will fulfill the requirements above.

Furthermore, you will be responsible for

- Setting up a vision for the service, how would it work in an ideal world?
- A realistic initial scope, how can we get something out quickly within the next 6 weeks?
- And, finally a rough plan for how to iterate on this initial version.

Additionally, you should be able to give a rough estimation of what resources (other developers, DevOps, etc) you would need.

Some important parts to take into consideration are:

1. **Deployment strategy**
    1. How do we deploy the service? This includes many parts like migrating the database, handling deploys when we have active life traffic, rollbacks, and more.
2. **Monitoring**
    1. How do we make sure that we can catch any issues in the service as quickly as possible?
    2. This also relates to the deployment strategy, how do we handle monitoring in relation to deploys?
3. **Cost optimization**
    1. How do we keep the costs down for the service and databases?
    2. It will initially be deployed only for smaller customers and should be cost-efficient for those.
    3. However, it should also become more cost-efficient as we grow towards larger customers
4. **Scalability**
    1. The service should be designed such that it can grow from handling a few thousand users to hundreds or even millions of users.
  
5. **Availability**
    1. The service can’t ever go down.
    2. How do we make sure that no matter what we can always handle the traffic?
    3. What strategies can we apply to handle all the potential issues we might see?
  
### Instructions
- The case should take a couple (2) hours to do.
- Draw out your architecture for the service and break it down into a long-term vision and a realistic initial step. Try to address all parts of the task.
- A visual illustration of the architecture is preferable to understand the solution.
- Remember, this will be used for evaluation. Make sure to showcase your competence and skills in the case.
- *Please submit the finalized case 24 hours before the following case interview in Teamtailor.*

Finally, be ready to explain your thinking and answer any follow-up questions on your solutions.
