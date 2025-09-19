# Asconababy-Text-To-Speech-Application

![IaC](https://img.shields.io/badge/IaC-Terraform-7B42BC?style=for-the-badge&logo=terraform)
![Cloud](https://img.shields.io/badge/Cloud-AWS-232F3E?style=for-the-badge&logo=amazonaws)
![Text-to-Speech](https://img.shields.io/badge/Text--to--Speech-API-4B5563?style=for-the-badge)
![Amazon Polly](https://img.shields.io/badge/Amazon%20Polly-TTS-F9A03C?style=for-the-badge&logo=amazon)
![AWS Lambda](https://img.shields.io/badge/AWS%20Lambda-Serverless-F58536?style=for-the-badge&logo=awslambda)
![API Gateway](https://img.shields.io/badge/API%20Gateway-Rest%20API-6B7280?style=for-the-badge&logo=amazonaws)
![Amplify](https://img.shields.io/badge/AWS%20Amplify-Frontend-F59E0B?style=for-the-badge&logo=awsamplify)


A serverless, infrastructure-as-code application that converts text to speech using Amazon Polly, deployed entirely with Terraform.

This project combines the power of AWS Lambda, API Gateway, S3, and Amplify to deliver a modern, full-stack solution — all without manually touching the AWS Console.

---


## Architecture

This diagram summarizes the full AWS-powered architecture, built and deployed using Terraform:

![Architecture Diagram](<img width="761" height="561" alt="Asconababy-Text-To-Speech-App Architecture drawio (1)" src="https://github.com/user-attachments/assets/5418c076-f5d0-4c8c-b860-17c57aa33336" />
)

---

## Features

- Converts user input text into `.mp3` audio using Amazon Polly
- Uploads audio to S3 and returns a presigned URL
- Fully managed through reusable Terraform modules
- Frontend hosted with Amplify (static HTML/CSS/JS)
- CORS-safe and ready for production integrations

---

## Screenshots

**Frontend UI – Welcome Screen**  
![Welcome UI](<img width="1366" height="768" alt="Screenshot (169)" src="https://github.com/user-attachments/assets/aaee67e8-c16f-4064-8071-59685b5bb3bb" />
)

**Frontend UI – Demo in Action**  
![In-Use UI](<img width="1366" height="768" alt="Screenshot (167)" src="https://github.com/user-attachments/assets/8f218475-238d-4e9e-a0f8-ca29b985e94c" />
)

**API Gateway – POST /convert route setup**  
![API Gateway](<img width="1366" height="768" alt="Screenshot (171)" src="https://github.com/user-attachments/assets/7ea26ad8-3886-4240-b688-3db1373dd700" />
)

**Amplify – Deployment screen**  
![AWS Amplify](<img width="1366" height="768" alt="Screenshot (168)" src="https://github.com/user-attachments/assets/7a042d0d-f03e-4745-a1be-81384d530b24" />
)

**CloudWatch – Lambda logs and execution time**  
![CloudWatch Log](<img width="1366" height="768" alt="Screenshot (174)" src="https://github.com/user-attachments/assets/94917a64-6de1-426a-bc1b-cabb60ab757f" />
)

**Terraform – Output after successful apply**  
![Terraform Apply Output](<img width="1366" height="768" alt="Screenshot (176)" src="https://github.com/user-attachments/assets/62081d63-1039-47d8-b1bb-fa8e82ff4512" />
)

**Terraform – Execution plan with resource changes**  
![Terraform Plan](screenshots/Terraform-Apply-2.png)

---

## Tech Stack

- **Terraform (modular structure)**
- **AWS Lambda (Python 3.12)**
- **Amazon Polly (Text-to-Speech)**
- **Amazon S3 (audio file storage)**
- **API Gateway (HTTP API v2)**
- **AWS Amplify (Frontend hosting)**
- **IAM (custom roles/policies)**
- **CloudWatch (log monitoring)**

---

## Folder Structure

```text
/terraform-text-to-speech-app/
├── main.tf
├── outputs.tf
├── terraform.lock.hcl
├── modules/
│   ├── amplify/
│   ├── api_gateway/
│   ├── lambda/
│   ├── iam/
│   └── s3/
├── lambda/
│   └── polly_handler.py
├── frontend/
│   └── index.html
├── .gitignore
├── README.md
└── screenshots/
    ├── Text-To-Speech-Welcome.png
    ├── Text-To-Speech-InUse.png
    ├── API Gateway.png
    ├── AWS Amplify.png
    ├── CloudWatch Log.png
    ├── Terraform-Apply-1.png
    ├── Terraform-Apply-2.png
    └── text-to-speech-Diagram.png
```



### Steps

```bash
# Clone this repo
git clone https://github.com/YOUR_USERNAME/terraform-text-to-speech-app.git
cd terraform-text-to-speech-app

# Zip your Lambda function
cd lambda
zip function.zip polly_handler.py -r
cd ..

# Deploy infrastructure
terraform init
terraform apply
```

### Manual Step (Frontend)
- Go to the Amplify Console
- Open the main branch
- Click "Manual deploy" and upload frontend.zip from the frontend/ folder

---


##  What I Learned

This project helped me deepen my understanding of:

- Writing clean, modular **Terraform code**
- Connecting multiple **AWS services** without using the AWS Console
- Deploying real apps with **Infrastructure as Code (IaC)**
- Handling **CORS** and integrating **API Gateway with Lambda**
- Monitoring and debugging with **CloudWatch logs**
- Structuring a full-stack project for future reuse and scaling

It also pushed me to improve how I document and present my work for technical audiences.


