### PrivateActivitiesinSF
How to make activities private for sensitive accts and contacts for confidential work in SF

[Original Post](http://www.acutedge.com/private-activities-in-salesforce-have-you-ever-needed-to-make-activities-private-while-sharing-the-parent-record/)

PRIVATE ACTIVITIES IN SALESFORCE: HAVE YOU EVER NEEDED TO MAKE ACTIVITIES PRIVATE WHILE SHARING THE PARENT RECORD?
I recently worked on a project where the Client needed to track private activities without making the contacts Private. Executive Director and Senior Managers worked with  high-net worth individuals and needed to track activities that were confidential in nature. Other users also worked with these Contacts, so we didn’t want to make them Private. If you have been in this situation you would know that salesforce provides a Private sharing setting (Organization-Wide Default) for Activity but it does not work if the Activity is related to a Public record. Here is the idea on AppExchange that illustrates the issue further: http://success.salesforce.com/ideaview?id=08730000000BrSoAAK

 

Another scenario that I have run into as a Nonprofit salesforce consultant –

 

You have Interns work with Contacts to host events and need to track their Activities; your Development team also tracks Tasks which they do not want interns to see.

 

 

jpeg1

 

 

In a nutshell, the Organization Wide Default (OWD) setting loses its meaning as soon as you relate the Task to a Contact or Account that is shared. Now you are left with the option to create these Accounts and Contacts as Private; meaning only the user creating them and users above in Role Hierarchy would see them. If other users need to work with the same Contact they would need to create a duplicate Contact…not ideal!!

 

 

 This is what you can do –

 Create a new profile for Senior Managers who would track confidential Activities and added those users to the profile.
 

Create a new custom field (Text Area) on Activities for storing Private Comments.
jpeg2

 

 

 Now click on the Field-Level Security button and assign the field to the desired profile (Senior Manager).
jpeg3

 

 Add the Private Comments field to the Task Page Layout.
jpeg4

 

Senior Managers will now see two comment fields on the Task layout. They can use the Private Comments field to track confidential comments that may only be seen by other users in the same Profile and the Comments field for public comments.
 

jpeg5

 

 

This is what other users will see for the same Task.
 

jpeg6

 

 

That’s it! Just so you know, other users can still see the Subject, and I found that to be good so they can see that an Activity was created by someone. If you really wanted, you could create a “private” Subject as well. Also, Field-Level Security does not prevent other users from searching on the Private Comments field. If needed, you can have Salesforce.com turn that on for you.

 

Here are a couple of other approaches that were considered –

Using a Custom Object for Private Activities
This may give you more control using OWD settings, however users will need to go to separate objects (relate lists) to create, update and view Activities.
You will not be able to leverage Task Reminders
