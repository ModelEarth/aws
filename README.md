# Amazon AWS

Also view our [AWS Amplify setup notes](amplify)  

## Getting started with Windows hosting on Amazon AWS  

**TIP 1: When hosting SQL with Windows, use RDS.**  
Hosting SQL on the same machine is significantly more costly because only the large virtual machines are supported.   

After spending several months configuring and testing our move to a large virtual machine, we worked with support to figure out how to downsize the machine when we discovered we were being charged $400/month during this time. To Amazon's credit, they agreed to apply charges to future hosting once we were ready to launch our new virtual machine.  

The AWS frontend do not provide an opportunity for customers to post reviews and feedback like Amazon.com, so we're sharing the following feedback and setup steps to help guide other users toward informed choices, some that the AWS support staff were not able to provide.  

**Recommendations for AWS**

One the server size page, display a message that RDS is the affordable alternative to hosting SQL on a single large OS where IIS also resides.  

Provide documentation on how to downsize after moving SQL to RDS. (You'll need to deactivate your IP address to avoid a vague error when making a snapshot.)  

Turning on billing notifications does not guarantee you will be notified as costs accure. Check your server billing at least twice a week to make sure you don't have any runaway charges.  