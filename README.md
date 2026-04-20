 ## AWS EC2 Static Website Hosting with IAM Access Control

## Deployed Project Link

http://52.203.7.222/
---

## EC2 Instance Details

* Instance Name: My Portfolio
* Instance Type: t3.micro
* OS: Amazon Linux 2023
* Web Server: Apache (httpd)
* Region: us-east-1
* Elastic IP: 35.174.188.54

---

## Project Description

This project demonstrates how to host a static website (HTML, CSS, JS) on an AWS EC2 instance and configure IAM users with different access levels.

The website is deployed using an Apache web server and is accessible publicly via an Elastic IP.

---

## IAM Users Configuration

###  User1 (No Permissions)

* No policies attached
* Cannot access EC2 services
* Shows **"not authorized"** error when trying to view instances

###  User2 (With EC2 Permissions)

* Policy attached: `AmazonEC2ReadOnlyAccess` & 'AmazonEC2FullAccess'
* Can view EC2 dashboard and instances
* Follows **Principle of Least Privilege**

---

##  Screenshots

### EC2 Instance Running

![EC2 Instance](./screenshots/ec2-instance.png)

<img width="1910" height="1078" alt="Screenshot 2026-04-19 143257" src="https://github.com/user-attachments/assets/207d7b9e-f807-4e14-aa88-3812f5a23fb0" />
<img width="1919" height="1079" alt="Screenshot 2026-04-19 143652" src="https://github.com/user-attachments/assets/80939cad-c052-496d-bf58-0b8f76eb47ed" />


### Website Hosted on EC2

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/615f351f-d60d-4633-893f-ec4b0eace4b0" />


---

###  User1 Login (No Access)

<img width="1920" height="1080" alt="Screenshot 2026-04-19 152309" src="https://github.com/user-attachments/assets/698f4cb7-484f-46ad-80e9-53cc191238dc" />

<img width="1920" height="1080" alt="Screenshot 2026-04-19 152353" src="https://github.com/user-attachments/assets/e8a2b2e7-21d3-44c4-8ab8-1c5d32f0c901" />


---

###  User2 Login (With Access)

<img width="1920" height="1080" alt="Screenshot 2026-04-19 152650" src="https://github.com/user-attachments/assets/29a80fdb-8d05-4274-bc94-7b793380177c" />
<img width="1917" height="1077" alt="Screenshot 2026-04-19 153410" src="https://github.com/user-attachments/assets/e1616386-1bf9-4b9b-9810-e14ce60756e1" />

## Challenges Faced
Initially used apt instead of dnf (Amazon Linux issue)
Faced issue with HTTP access due to security group configuration
Confusion in IAM permissions setup
Region mismatch while checking EC2 instances


##  Learning Outcomes

* Learned how to launch and configure EC2 instances
* Understood difference between Public IP and Elastic IP
* Installed and configured Apache web server on Amazon Linux
* Implemented IAM users with role-based access control
* Understood AWS security best practices

---

## ✅ Conclusion

Successfully deployed a static website on AWS EC2 and implemented IAM-based access control with different permission levels for users.
