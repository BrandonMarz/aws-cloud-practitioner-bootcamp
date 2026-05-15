
This is the #1 risk scenario. 
"Security OF the Cloud" (AWS) or "Security IN the Cloud" (Customer).

* Scenario: Data is leaked from an S3 bucket because it was set to "Public."
    * Risk Owner: Customer. AWS provides the "Block Public Access" tool, but you chose to turn it off.
* Scenario: A physical server in an AWS data center is stolen.
    * Risk Owner: AWS. They are responsible for physical security (cameras, guards, fence).
* Scenario: An EC2 instance is hacked because the OS wasn't patched.
    * Risk Owner: Customer. AWS provides the infrastructure; you must manage the "Guest OS."

2. Identity and Access Management (IAM) Risks
* Scenario: A developer leaves the company, but their login still works.
    * Solution: Use IAM Groups/Roles and perform regular Access Audits.   
* Scenario: A root user account is compromised because it only had a password.
    * Solution: Enable MFA (Multi-Factor Authentication). Never use the root account for daily tasks.   
* Scenario: Hardcoded "Access Keys" are found in a public GitHub repo.
    * Solution: Use IAM Roles for EC2 instances instead of static keys.   

3. Infrastructure & Availability Risks
* Scenario: A lightning strike hits a data center, and your website goes down.
    * Risk: Single Point of Failure.
    * Solution: Deploy across multiple Availability Zones (AZs).   
* Scenario: An entire region (e.g.,Cape Town) has a massive outage.
    * Solution: Multi-Region deployment for "Business Continuity."

4. Data Protection Risks
* Scenario: Sensitive customer data is stored in plain text.
    * Solution: Use AWS KMS (Key Management Service) to manage encryption keys.   
* Scenario: You need to find "hidden" PII (names, credit card numbers) in thousands of files.
    * Solution: Amazon Macie. It uses AI to scan S3 for sensitive data.   

5. Compliance & Auditing Risks
* Scenario: An auditor asks "Who changed the firewall rules at 3:00 AM?"
    * Solution: AWS CloudTrail. It logs every API call (who, what, when).
* Scenario: You need to see if your architecture meets PCI-DSS or HIPAA standards.
    * Solution: AWS Artifact. This is the portal for downloading AWS compliance reports.
