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


## Admin account on RDS

We looked into how to setup Windows authentication for RDS like we have now on Darby and the process involves setting up Active Directory and domain controllers, all of which is handled behind the scenes. However, they gave an example of the monthly cost for a basic setup and it’s $288/month - way too much. So, we just stick with using the admin account.  

https://aws.amazon.com/directoryservice/pricing/

 
Also, we found that the admin account does not have a sysadmin role. However, it seems to have enough permissions for us to do our work (so far) without having too many permissions where we could mess up how RDS works if we inadvertently change something. We don’t know what the sa password is, that’s not available when setting up RDS so we can’t change this. Hopefully, this won’t cause any problems.

 
