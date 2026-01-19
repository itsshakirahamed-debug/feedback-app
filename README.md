# feedback-app
A serverless feedback application using aws

---

## ⚙️ How It Works

1. User submits feedback from the website form
2. The frontend sends a POST request to API Gateway
3. API Gateway triggers Lambda
4. Lambda validates the request and stores it in DynamoDB
5. Success response is shown on the website

---

## 🚀 Deployment Steps (High Level)

### 1) Create DynamoDB Table
- Table Name: `FeedbackTable`
- Partition Key: `feedbackId` (String)

### 2) Create Lambda Function
- Function Name: `SaveFeedbackLambda`
- Runtime: Python 3.x
- Add permission to write to DynamoDB (IAM Role)

### 3) Create API Gateway
- Route: `POST /feedback`
- Integration: Lambda function
- Enable CORS:
  - Allow origin: `*`
  - Methods: `POST, OPTIONS`
  - Headers: `content-type`

### 4) Create S3 Website
- Upload `index.html`
- Enable static website hosting
- Make bucket public (for website access)

---

## 🧪 Demo

### 🌐 Website URL
- `http://feedback-app-shakir123.s3-website.eu-north-1.amazonaws.com`

### 🔗 API Endpoint
- `https://y5a5tu5190.execute-api.eu-north-1.amazonaws.com/prod/feedback`




## 💡 Learnings

- Built and deployed a complete **serverless application**
- Understood AWS service integrations (S3 + API Gateway + Lambda + DynamoDB)
- Learned about **CORS configuration** and API deployment stages
- Gained hands-on experience with AWS cloud architecture

---

## 🧑‍💻 Author

**Shakir Ahamed**  
Cloud / AWS Learner  

