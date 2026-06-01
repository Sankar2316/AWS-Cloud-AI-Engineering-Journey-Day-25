# 🚀 Day 25 – AWS Event-Driven Architecture

---

## 📌 Overview

On Day 25, I explored Event-Driven Architecture using AWS services:

- Amazon EventBridge
- Amazon SQS
- Amazon SNS
- AWS Lambda
- CloudWatch

This architecture is widely used in:
- Microservices
- Real-time systems
- AI pipelines
- E-commerce platforms
- Serverless applications

---

## ⚡ What is Event-Driven Architecture?

Event-Driven Architecture (EDA) is a design pattern where services communicate using events.

Instead of direct communication:

Service A → Event → Service B

This improves:

✅ Scalability
✅ Reliability
✅ Loose Coupling
✅ Faster Processing

---

## 🔑 Core AWS Services

| Service | Purpose |
|----------|----------|
| EventBridge | Event Routing |
| SNS | Publish Notifications |
| SQS | Message Queue |
| Lambda | Process Events |
| CloudWatch | Monitoring |

---

## 📨 Amazon SNS

Amazon SNS (Simple Notification Service) is used for:

- Email Alerts
- SMS Notifications
- Event Broadcasting

### Example

Order Placed
↓
SNS Topic
↓
Email + SMS + Lambda

---

## 📬 Amazon SQS

Amazon SQS (Simple Queue Service) stores messages safely until processing.

### Benefits

- Decouples applications
- Handles traffic spikes
- Reliable message delivery

---

## 🌉 Amazon EventBridge

EventBridge connects AWS services using events.

### Example

EC2 Instance Created
↓
EventBridge Rule
↓
Lambda Trigger

---

## ⚙️ Event Processing Workflow

Customer Action
↓
EventBridge
↓
SNS Topic
↓
SQS Queue
↓
Lambda Function
↓
Database Update

---

## 🌐 Real-World Project

### Smart Student Notification System

Features:

- Student registers
- EventBridge captures event
- SNS sends email
- SQS stores event
- Lambda processes request
- DynamoDB updates records

---

## 🔐 Security Features

- IAM Roles
- Encryption
- Secure Event Routing
- Monitoring
- Access Control

---

## 📊 Monitoring

CloudWatch Monitors:

- Event failures
- Queue size
- Lambda execution
- Notification status

---

## 💻 Sample Lambda Code

```python
def lambda_handler(event, context):
    print("Event Received")
    return {
        "statusCode": 200
    }
