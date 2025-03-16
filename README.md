### **README for AWS Cloud Newsletter System**

# **AWS Cloud Newsletter System**
An automated newsletter-based email notification system using AWS services for efficient and personalized email delivery.

---

## **Overview**
This project leverages AWS services to create a scalable, reliable, and automated email notification system for delivering newsletters. Key AWS tools such as S3, Lambda, API Gateway, SES, and DynamoDB are used to manage subscriptions, content delivery, and performance tracking.

---

## **Features**
✅ Fully automated newsletter delivery  
✅ Personalized content based on subscriber preferences  
✅ Reliable email delivery with bounce and error handling  
✅ Scalable architecture to accommodate growing subscriber lists  
✅ Integrated performance tracking (open rates, click-through rates, etc.)  

---

## **Tech Stack**
- **AWS S3**: Stores newsletter templates and static assets  
- **AWS Lambda**: Automates email dispatch and data handling  
- **API Gateway**: Facilitates communication between users and AWS Lambda  
- **Amazon SES (Simple Email Service)**: Ensures secure and scalable email delivery  
- **DynamoDB**: Manages subscriber data efficiently  

---

## **Installation & Setup**
1. **Clone the Repository**  
   ```bash
   git clone https://github.com/your-username/email-notification-system.git
   cd email-notification-system
   ```

2. **AWS Configuration**  
   - Create and configure an **S3 Bucket** for storing newsletter templates.  
   - Set up **AWS Lambda** functions for handling email subscriptions and dispatch.  
   - Use **API Gateway** to manage endpoints.  
   - Configure **SES** for sending emails.  
   - Deploy a **DynamoDB** table to store subscriber data.  

3. **Environment Variables (.env file)**  
   ```
   AWS_ACCESS_KEY_ID=YOUR_AWS_ACCESS_KEY
   AWS_SECRET_ACCESS_KEY=YOUR_AWS_SECRET_KEY
   AWS_REGION=ap-south-1
   DYNAMO_DB_TABLE_NAME=Subscribers
   SES_SENDER_EMAIL=your-verified-email@example.com
   ```

4. **Deployment**  
   Deploy your Lambda functions using AWS Console or AWS CLI.

---

## **Usage**
1. **Subscribe to Newsletter**  
   - Users submit their email addresses via the website (S3 hosted).  

2. **Email Storage and Automation**  
   - Subscriber data is stored in DynamoDB.  
   - The Lambda function automatically fetches the latest content from S3 and dispatches the email through Amazon SES.  

3. **Performance Tracking**  
   - AWS CloudWatch Logs tracks the success, errors, and engagement statistics.  

---

## **Project Structure**
```
/public
    └── subscription-form.html
/src
    ├── saveSubscriberEmail.js
    ├── sendNewsletterBulk.js
    └── emailTemplates/
        └── sample-newsletter.html
/aws
    ├── api-gateway.yaml
    ├── lambda-functions/
    └── dynamodb-schema.json
```

---

## **Sample Test Data**
✅ **Sample Subscriber Email**: `user123@example.com`  
✅ **Sample Newsletter Topic**: "Cosmic Chronicles: NASA’s Latest Lunar Mission"  

---

## **Screenshots**
🚀 Subscriber Form Interface  
📬 Sample Newsletter Delivery  
📊 CloudWatch Analytics Tracking  

---

## **Contributors**
- **Trisha Rami** – Project Lead  
- Open for Collaboration  

---

## **License**
This project is licensed under the **MIT License**.  

---

