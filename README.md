# AWS Resources

Best practices, Well-architected audits, account setup. 

Resources (Startups and new accounts)

- [Get Started with AWS](https://getstarted.awsworkshop.io/00-intro.html)
- [AWS for Startups](https://youtu.be/U3VSJhaC4kc)
- [AWS Well-Architected for Startups ](https://www.youtube.com/watch?v=GhTC-pMgOjc&list=PLhr1KZpdzukdc8hT9hCF8hwfWkYAX-frO)
- [AWS for Startups: 5 Practical Tips for Small Businesses Building on AWS](https://www.lastweekinaws.com/blog/aws-for-startups-5-practical-tips-for-small-businesses-building-on-aws)
- [AWS Activate program](https://aws.amazon.com/activate/) Build and scale with up to $100,000 in AWS Activate credits 
- [Build on AWS for Startups](https://youtu.be/Gql3wNTL5TU)
- [Production Readiness Checklist](https://gruntwork.io/devops-checklist)
- [Well-Architected Framework](https://github.com/mguery/aws-well-architected/blob/main/well-architected-checklist.md)


## How to set up AWS account
1. [Create an AWS account](https://aws.amazon.com/getting-started/guides/setup-environment/module-one/)
2. [Secure your AWS account](https://aws.amazon.com/getting-started/guides/setup-environment/module-two/)
3. [Set up AWS Command Line Interface](https://aws.amazon.com/getting-started/guides/setup-environment/module-three/)

## [New AWS Account Setup Checklist and Best Practices](https://katalysttech.com/blog/new-aws-account-setup-checklist-and-best-practices)
1. Use a distribution/group email address to register for the account - The email used to create the AWS account has complete control of all AWS resources. Consider creating an account with a group/distribution email address with all the people who should have root access.
If you have already registered for an account with an individual email, you can update the root user name with a distribution list.
2. Enable Multi-Factor Authentication (MFA) on Root Account - As a best practice, all root accounts should enable Multi-Factor Authentication (MFA). Configure using a virtual MFA device like Microsoft or Google Authenticator.
You can take a screenshot of the QR code and save it in a secure location or as an attachment in your password manager.
3. Create a password policy - Customize your password policy that aligns with your organizational password policies. Ensure that:
  – Increase the password length to at least 14 characters
  – Require at least one upper case alphabet, number, and a symbol
  – Disallow password reuse and set the password reuse to 24.
4. Create IAM Users with Console Login - Avoid using the root account for day-to-day operations. Create IAM users with admin access for all administrative privileges. Assign users to groups rather than assigning permissions directly to the users. Enable Multi-Factor authentication uses for all console users.
5. Activate IAM user access to billing information - AWS billing information is available only to the root user. Activate billing information access to IAM users so that admins can access the billing dashboard.
  – Sign in to the AWS Management Console with your root account credentials.
  – In the top navigation bar, choose an account name, and then select My Account
  – Click on Edit Next to IAM User and Role Access to Billing Information
  – Select ‘Activate IAM Access’ and click ‘Update.’
6. Monitoring Infrastructure Costs with AWS Billing Alarm and CloudWatch - AWS bills add up quickly if you do not keep a tab on the services you provisioned. AWS billing alerts leverages CloudWatch to provide proactive alerting and alarms on your total AWS charges. You can set the alarm if your bill has reached or exceeded a specific amount.
7. AWS Support Plan - Subscribe to get business or enterprise support plans for any accounts that run production workloads. You can run a complete set of checks with a trusted advisor, 24 X7 support over phone, email, and chat access to AWS cloud engineers.
8. Review AWS Trusted Advisor Settings - The Trusted advisor monitors your AWS environment and provides recommendations to align with the AWS well-architected framework. The trusted advisor offers guidance in the following five categories.
  – Cost Optimization
  – Performance
  – Security
  – Fault Tolerance
  – Service Limits
It is recommended to have at least business support to leverage the full features of the trusted advisor.
9. Enable AWS Config - The first step to securing your environment is to create an asset inventory. AWS Config enables you to assess, audit, and evaluate configurations of the AWS services deployed in the account. AWS Config continuously monitors and records your AWS configurations. You can get a count of all the resources across the account.
10. Enable CloudTrail - CloudTrail creates an audit trail of all the actions performed on your account. The primary use of CloudTrail is Governance, Compliance, Security controls, andCloudTrail logs all success and failure events of all requests from the AWS Console, CLI, and SDK.


