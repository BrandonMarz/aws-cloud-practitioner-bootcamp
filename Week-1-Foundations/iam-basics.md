IAM (Identity and Access Management) is the foundation of AWS security. It allows you to control who can access what within your AWS account.
IAM: The Big Three
Users: Long-term credentials for people.
Groups: Logical collections of users to manage permissions at scale.
Roles: Temporary credentials for services (like an EC2 instance) or external users. Use these instead of hardcoded keys.

Permissions & Security
Principle of Least Privilege: Give only what is needed, nothing more.

JSON Policies: The code that defines "Who" can do "What."

Root User: The "God Mode" account. Use it once to set up, then lock it with MFA and stop using it.

MFA: The single most important security step for any IAM user.

The Shared Responsibility Model
Think of it as an apartment building:

AWS (The Landlord): Responsible for the "Building" (Security OF the cloud). Physical locks, electricity, plumbing, and the server hardware.

Customer (The Tenant): Responsible for the "Furniture" (Security IN the cloud). Your data, your firewall settings, and your OS updates.
