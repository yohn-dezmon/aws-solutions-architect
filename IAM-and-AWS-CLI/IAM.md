# IAM

Identity Access & Management  
Global service  

JSON Policies determine permissions for users or groups.  
Groups cannot contain other groups.  
Groups are composed of users.  
users don't HAVE to belong to a group.  

Root account should not be used/shared.  
Least priviledge principle.  

IAM Hands On:  
- we created a user John 
- we assigned it to "admin" group
- we gave that group the AdministratorAccess policy, which propagated to the John user 
- we assigned an alias for the account 

Policy Inheritance:
- policies are applied to groups typically 
- they propagate to all users in a group
- a policy given to a specific user is an inline policy 

Policy Structure:
- ID (optional)
- Version : "2012-10-17"
- Statements: one or more. 
- determines a permission! 


Statements:
- sid -- optional id
- effect: either `Allow` or `Deny`
- Resource: the resource that will be affected
- condition (optional)
- Principal: user/role that will be given the permission 
- Action: e.g. `s3:GetObject`, determines the allow/deny action. 



