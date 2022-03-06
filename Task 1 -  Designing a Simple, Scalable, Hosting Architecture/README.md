You are a solutions architect at AWS. A customer has contacted you because they are having some problems with the way their web application is currently hosted:

Hi,

My name is Lilly Sawyer and I am the co-founder and CTO of Fastier, the online tool that makes organizing things fast.

You may have seen that we have been in the news recently and have been experiencing some big growth as a result. 
Unfortunately, this means we’ve been having some difficulties with our website. 
The response times can be slow during peak periods and sometimes we even have server crashes when it runs out of memory. 
We also experience some downtime during deployments and don’t have a disaster recovery plan. 
Based on our current trajectory, we predict we’re going to see consistent linear growth for a while.
Our application is a SPA React Application backed by Python and Flask, with PostgreSQL as a database. 
It all runs off a single AWS EC2 instance currently (t3.medium, 4GB of RAM).

Can you design an architecture for us that will alleviate the problems we’re experiencing? We are not on a strict budget right now, but at the same time, it’s not unlimited.

Kind regards,
Lilly

As an aside, please note that Elastic Beanstalk is not the only product that we could recommend for this customer. 
AWS is an open platform and encourages creativity when building solutions. 
We need to be aware of the pros and cons of each solution and how they will best fit each customer.
Other options like Lambda or Fargate can be more complex to set up. 
Lightsail and EC2 can be easy but they don’t provide that automatic scaling; the customer can end up paying more because they are running virtual machines that are often not at capacity. However, each of these services also has its own advantages, and depending on the application that’s being built we can provide different recommendations and discuss the options more in-depth with the customer before coming up with the final design.

The services we will use are:

Route 53

Elastic Load Balancing

Elastic Beanstalk with Autoscaling EC2 Group

RDS

S3

CodePipeline

An additional availability zone for redundancy is proposed but is not necessary.

Your task is to draft an email reply to Lilly Sawyer. In the email, you are showing your architecture diagram for the first time (see additional resources). You will need to explain what each part of the architecture is and why it was chosen. Also briefly explain how the costs are calculated and how they may vary month-to-month. Remember you don’t need to give concrete numbers, just an overview.
