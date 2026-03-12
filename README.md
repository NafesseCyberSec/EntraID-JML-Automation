# EntraID-JML-Automation
Manual access management doesn't scale. When you have thousands of employees joining, changing roles, and leaving, you need automation. JML automation + RBAC/ABAC ensures the right people get the right access at the right time—automatically.

What Are Dynamic Groups?

Dynamic groups automatically add/remove members based on user attributes. When someone's department changes in HR, they automatically move to the correct group—no manual work!

-Create a Dynamic Group-


1.

Go to Groups

In Entra ID, click "Groups".


2.

Click "New group"


<img width="600" height="312" alt="image" src="https://github.com/user-attachments/assets/10172643-8cf9-49a1-bf6c-ea23f29d0543" />



3.

Configure basics

Group type: "Security"

Group name: "Auto-Engineering-Team"

Membership type: "Dynamic User"

<img width="600" height="391" alt="image" src="https://github.com/user-attachments/assets/3124c212-2f25-4d04-a406-2c4ed8ef2405" />



4.

Add dynamic query

Click "Add dynamic query".


5.

Build the rule
Set:

Property: department

Operator: Equals

Value: Engineering Or use advanced syntax:

(user.department -eq "Engineering")


6.

Validate

Click "Validate Rules" to test against existing users.


7.

Create
Click "Save" → "Create".
