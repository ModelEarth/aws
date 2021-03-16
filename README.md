# Amazon AWS

## Amplify App Notes

View our [Amplify setup notes](amplify)  

## Getting started with Windows hosting on Amazon AWS  

Generally the Amazon AWS controls are not geared toward saving customers money, so you'll need to be savvy and avoid the default settings.  When hosting SQL with Windows, use RDS. Hosting SQL on the same machine is significantly more costly.  

Unlike Amazon.com where customer reviews and feedback help guide the user toward informed choices, you'll find a dirth of collaboration and constructive guidance in the AWS ecosystem. Buyer beware.  

### Recommendations for a more customer-centric AWS for greater user retention

You'll find there is no information stating that using RDS is the affordable alternative to hosting SQL, rather than using the same server as IIS.  

There is no documentation on how to downsize after moving SQL to RDS. (You'll need to deactivate your IP address to avoid a vague error when making a snapshot.)  

Also beware, turning on notifications does not guarantee you will be notified as costs accure. Check your server billing at least twice a week to make sure you don't have any runaway charges.  

View our [Windows server setup notes](../setup/)