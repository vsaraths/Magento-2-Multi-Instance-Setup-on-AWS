# Magento-2-Multi-Instance-Setup-on-AWS
Magento 2 Multi-Instance Setup on AWS
This guide provides a step-by-step approach to deploy Magento 2 across four AWS instances for a scalable environment. Designed for AWS Free Tier, each instance runs Debian 11 with dedicated services.

📋 Table of Contents
Prerequisites
Architecture Overview
Instance Setup
Database Server (MySQL)
Elasticsearch Server
Web Server (Nginx, PHP, Magento)
Varnish Server
Post-Installation
Troubleshooting
Cleaning Up

🛠 Prerequisites
AWS Account with Free Tier eligibility.
SSH Key Pair created in AWS.
Basic CLI knowledge.

🌐 Architecture Overview
Instance 1: MySQL 8 (Private IP: DB_IP)
Instance 2: Elasticsearch (Private IP: ES_IP)
Instance 3: Nginx, PHP 8.1, Redis, Magento 2 (Private IP: WEB_IP)
Instance 4: Varnish (Public IP: VARNISH_IP)


🚀 Instance Setup
Launch four Debian 11 t2.micro instances. Assign security groups:
Database: Allow MySQL (3306) from WEB_IP.
Elasticsearch: Allow HTTP (9200) from WEB_IP.
Web Server: Allow HTTP (80), HTTPS (443), SSH (22).
Varnish: Allow HTTP (80), HTTPS (443), SSH (22).

