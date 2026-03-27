# AWS IIoT Data Pipeline: OT-to-IT Architecture

![AWS](https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazon-aws&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![IoT](https://img.shields.io/badge/IoT-FF9900?style=for-the-badge&logo=awslambda&logoColor=white)

## 🌐 View the Interactive Case Study
**[Click here to view the live Solution Brief](https://roy-chambers-gb.github.io/aws-iiot-data-pipeline/)**

---

## 🏗️ Project Overview
This repository contains the architecture and implementation logic for a production-grade **Industrial IoT (IIoT)** data pipeline. The solution bridges the gap between **Operational Technology (OT)** and **Information Technology (IT)**, focusing on secure ingestion, multi-tenant isolation, and real-time critical alerting.

### **Key Architectural Wins:**
* **Security:** End-to-end encryption using **X.509 Mutual TLS (mTLS)** for hardware-level device identity.
* **Scalability:** Asynchronous buffering via **Amazon Kinesis** to handle high-velocity industrial data bursts.
* **Multi-Tenancy:** Data isolation achieved through **Partition Key sharding** (tenant-based routing).
* **Alerting:** Millisecond-level threshold evaluation using serverless **AWS Lambda** and **SNS**.

---

## 🛠️ Technology Stack
* **Edge:** Python-based Gateway Simulator (mTLS enabled).
* **Ingestion:** AWS IoT Core (MQTT / Port 8883).
* **Data Stream:** Amazon Kinesis Data Streams.
* **Compute:** AWS Lambda (Python 3.x).
* **Notifications:** Amazon SNS (Simple Notification Service).
* **Region:** London (`eu-west-2`) for UK data residency compliance.

---

## 📊 Architecture Diagram
![Architecture Diagram](OT-to-IT%20Data%20Pipeline.png)

---

## 📝 Architectural Decision Records (ADR)
1. **Why Kinesis?** To provide a resilient buffer against "bursty" industrial data, preventing downstream bottlenecks and ensuring 100% data durability.
2. **Why mTLS?** To meet the highest industrial security standards (**ISA/IEC 62443**) for device-to-cloud communication.
3. **Why Serverless?** To achieve a cost-optimised "pay-as-you-go" model with zero overhead during factory downtime.

---

## 🚀 Future Roadmap
* **Data Lake:** Implementing Kinesis Firehose for long-term S3 storage and Athena-based auditing.
* **Predictive Maintenance:** Integrating Amazon SageMaker for machine failure forecasting.
* **Visualisation:** Building real-time operational dashboards in Amazon QuickSight.

---

## 📧 Contact & Networking
**Roy Chambers** [LinkedIn Profile](https://www.linkedin.com/in/roy-chambers-82810018/)  
*Solution Architect specialising in AWS Cloud & Industrial IoT Integration.*