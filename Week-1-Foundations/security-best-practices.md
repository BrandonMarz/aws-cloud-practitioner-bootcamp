1. Identity (IAM)
MFA: Mandatory for Root; recommended for everyone.

Roles over Keys: Use IAM Roles for services; avoid long-term Access Keys.

Least Privilege: Grant only the minimum permissions needed.

Groups: Assign permissions to groups, not individuals.

2. Infrastructure
Security Groups: Act as virtual firewalls (Allow-only rules).

Private Subnets: Keep databases away from the public internet.

Shield & WAF: Protect against DDoS and web exploits (SQLi/XSS).

3. Data Protection
KMS: The "one-stop shop" for Encryption Keys.

S3 Security: Use "Block Public Access" by default.

TLS/SSL: Encrypt data "in transit" (moving between points).

4. Monitoring (The "Big Three")
CloudTrail: Tracks Actions (Who did what?).

GuardDuty: Identifies Threats (Intelligent detection).

Config: Tracks Changes (Configuration history).

The "Golden Rules"
Root User: Delete its keys; stop using it after setup.

Shared Responsibility: AWS secures the hardware; You secure the data.

Secrets Manager: Never hardcode passwords; use a vault.
