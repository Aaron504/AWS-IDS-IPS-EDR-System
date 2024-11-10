# AWS IDS IPS System
<p align="center">

![Screenshot 2024-11-10 153848](https://github.com/user-attachments/assets/98dbcc73-50e7-42bb-b5b9-00fad742a747)

</p>

In this project, I designed and implemented a robust Intrusion Detection and Prevention System (IDS/IPS) within the AWS cloud environment to detect, monitor, and mitigate security threats. Leveraging AWS-native security services such as GuardDuty, WAF, and Amazon Inspector, I created a layered defense system capable of identifying unauthorized access attempts, SQL injection, XSS attacks, and vulnerabilities in real-time. Through the integration of CloudTrail, VPC Flow Logs, and Route 53 DNS Query Logging, I achieved comprehensive visibility across network traffic, user actions, and DNS requests. Findings were centralized in AWS Security Hub, with CloudWatch Alarms set up for real-time alerts, providing immediate awareness of critical threats. This project demonstrates my expertise in cloud security and proactive threat management, showcasing my ability to build and manage secure cloud infrastructures on AWS.




<h2>Environments and Technologies Used</h2>

- AWS GuardDuty
- AWS WAF (Web Application Firewall)
- Amazon Inspector
- AWS CloudTrail
- VPC Flow Logs
- Amazon Route 53 Resolver Query Logging
- AWS CloudWatch
- AWS IAM (Identity and Access Management)


<h2>High-Level Deployment and Configuration Steps</h2>

- Step 1 - Set Up AWS GuardDuty
- Step 2 - Configure AWS WAF for Protection
- Step 3 - Use Amazon Inspector for Vulnerability Detection
- Step 4 - Test Simulated Attacks

<h2>Deployment and Configuration Steps</h2>

- Step 1: Set Up AWS GuardDuty
- 1. Activate GuardDuty:

Go to the GuardDuty console.
Enable the service for your account and region.

![Screenshot 2024-11-09 202018](https://github.com/user-attachments/assets/1f267158-54b2-4cfb-98ea-4dfa5ee5450c)

- 2. VPC Flow Logs

VPC Flow Logs capture information about IP traffic going to and from network interfaces in your VPC. GuardDuty uses this data to detect suspicious network activity.

![Screenshot 2024-11-10 131008](https://github.com/user-attachments/assets/e5ce963f-e3e9-4932-a906-dfa866005e62)
![Screenshot 2024-11-10 131046](https://github.com/user-attachments/assets/a04f9c8b-296c-467c-bb4a-e2fef5592a1a)

- 2. AWS CloudTrail Logs

CloudTrail logs record API calls within your AWS account, providing insight into user activity. GuardDuty uses these logs to detect unauthorized API calls, privilege escalations, and other suspicious actions.

![Screenshot 2024-11-10 132946](https://github.com/user-attachments/assets/bdfba531-ddd6-4c68-9b70-0d52a0725374)
![Screenshot 2024-11-10 133016](https://github.com/user-attachments/assets/1468f38c-2e27-4603-9288-fd23149fe716)
![Screenshot 2024-11-10 134409](https://github.com/user-attachments/assets/1ae25837-6630-47f9-82bc-d5e67ae8b053)

- 3. DNS Logs (Route 53 Resolver Query Logging)

DNS logs track DNS queries, which can help identify malware communications and data exfiltration attempts. GuardDuty can use these logs for threat detection if you enable DNS query logging.

![Screenshot 2024-11-10 135411](https://github.com/user-attachments/assets/212d2b1b-2e1c-4de5-8f7f-23db283c3c02)
![Screenshot 2024-11-10 140217](https://github.com/user-attachments/assets/d608b3d9-afd6-4521-898c-c73d071c463e)
![Screenshot 2024-11-10 140237](https://github.com/user-attachments/assets/0beea06f-41c1-4b57-9253-f02468888e7b)
![Screenshot 2024-11-10 140948](https://github.com/user-attachments/assets/61b04eb2-6b0c-4418-ad5d-41cbaacbbe2d)

- Step 2: Configure AWS WAF for Protection

AWS WAF (Web Application Firewall) filters traffic to protect your web applications from attacks.

- 1. Set Up WAF:

Go to the WAF console and create a WebACL.
Attach this WebACL to an Application Load Balancer, CloudFront distribution, or API Gateway.

![Screenshot 2024-11-10 143334](https://github.com/user-attachments/assets/a909cae9-b5d9-4c69-ae8c-2c33ec4d4c57)

- 2. Add Rules
  - Use managed rule sets that AWS offers (like AWS Managed Rules) or create custom rules.
  - Configure rules for common attacks (e.g., SQL injection, XSS).
  - Enable logging for your WAF to CloudWatch for monitoring.
  ![Screenshot 2024-11-10 150157](https://github.com/user-attachments/assets/092a3b27-14a5-465e-8df9-ed842831093f)
  ![Screenshot 2024-11-10 150214](https://github.com/user-attachments/assets/70c3f547-05d7-49c5-82c2-abe1dadfc0f9)

- Step 3: Use Amazon Inspector for Vulnerability Detection

Amazon Inspector helps identify vulnerabilities in your EC2 instances and Lambda functions.

![Screenshot 2024-11-10 151917](https://github.com/user-attachments/assets/4efb2ddc-0f7d-4b4d-88ce-6848621b9e7f)

- Step 4: Test Simulated Attacks

![Screenshot 2024-11-10 152734](https://github.com/user-attachments/assets/813e6e31-4c24-473e-8f8d-0c0b3bb0cde7)
![Screenshot 2024-11-10 152909](https://github.com/user-attachments/assets/c479b5c7-e91f-4b65-9379-013138eb177a)
![Screenshot 2024-11-10 152921](https://github.com/user-attachments/assets/0de4617a-e0fd-44f2-8db3-62f93353bbaf)



















