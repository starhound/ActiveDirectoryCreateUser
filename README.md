# ActiveDirectoryCreateUser
A Powershell script to easily create new users in AD and send email confirmations.

This script will perform several actions when ran:

It will attempt to elevate itself to Admin status on the local system. 

Then it will enable PS-Remote on said system. 

Once enabled, it will attempt to connect to your Domain Controller. 

Once connected, it gathers some input (first name, last name, email address) and creates a new user in Active Directory, using a temporary password, with information from the input given.

Once created, it will attempt to send a confirmation email to whoever you set.

Some notes: Requires logon to the domain controller as well as the mail server. Anywhere in the script that you see "YOUR_", you need to input your own network information (such as your domain controller host name or mail server url).
