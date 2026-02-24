## Understand the Project Background ( Real-World Production Environment Simulation ) 

You are working as a **System Administrator and DevOps Engineer** in a cloud-based service company.
Your company has received a new client:
A `Jewelry & Diamond business company` that is expanding into online operations. 
They want to build and host their website infrastructure professionally on cloud.
You are assigned as the **DevOps Lead**, and you have a team with mixed knowledge levels.
Your responsibility is to design, configure, and deliver a complete production-ready infrastructure for the client.

---
# Question-1 – Static Web Hosting (Non-Secure & Secure)

The client wants to start with a simple static website (no database).
They want their business to be visible publicly through their purchased domain.
You must deploy everything on AWS Cloud.

### Server Requirements

Create and configure the following infrastructure:

* `Instance Type`: **t2.medium** (2 vCPU + 4GB RAM)
* `Storage`: Minimum 10 GB
* `Operating System`: RHEL 9
* `Region`: Mumbai

Deploy a simple static monolithic web application.

---
### Domain & Subdomain Configuration

The client has already purchased the domain:
**RichShop.com** (valid for 3 years)

Now configure the following:
* `www.richshop.com` → Should display the main website
* `mail.richshop.com` → Should display shop mail site content
* `photos.richshop.com` → Should display jewelry design photo portfolio content

Make sure all DNS records are configured properly.

---
### Enable HTTPS (Secure Hosting)

The client now wants secure access for all websites.

Configure SSL so the following URLs work properly:

* [https://www.richshop.com](https://www.richshop.com)
* [https://mail.richshop.com](https://mail.richshop.com)
* [https://photos.richshop.com](https://photos.richshop.com)

All domains and subdomains must open securely each domain and sub-domain `using HTTPS with dedicated different DocumentRoot Directory contents`.

---
#  Question-2– Secure Dynamic Three-Tier Architecture (WordPress + MySQL)

After some time, the client decides to upgrade the website.
Now they want:
* Login-based website
* Customer registration
* Metadata storage
* Secure database integration

Note: You can simply use pre-build wordpress themes for this. Do not need to write code from scratch here. 

You must redesign the static website infrastructure into a **Database Based Three-Tier Architecture**:
1. Web Tier
2. Application Tier
3. Database Tier

---
### What you Deploy:
* WordPress as application
* MySQL as database
* Secure communication between tiers


Ensure the following URLs work:
* [https://www.richshop.com](https://www.richshop.com) → WordPress main site
* [https://mail.richshop.com](https://mail.richshop.com) → Mail site
* [https://photos.richshop.com](https://photos.richshop.com) → Photo portfolio

The database must store:

* User login details
* Metadata
* Website content

Implement proper security and isolation between layers.

---

# Question-3 – DNS Server Setup

Your company also provides DNS services.
The client wants their domain to resolve using your company’s DNS server instead of third-party DNS.


### Your DNS Work
Set up a DNS server from scratch.
After configuration: When someone runs:
```
nslookup www.richshop.com
```

It must resolve using your configured DNS server.
Ensure proper:

* Forward lookup zone
* A records
* Subdomain records

---

# Question-4 – NFS Server & Backup Strategy

During a review meeting, the client raised concern about data safety.

They want:
* Daily backup of database
* Backup timing: 11:00 PM (Low traffic time)
* Compressed format
* Proper naming convention with timestamp

### Your NFS Work

Implement a Cloud based NFS Solution:

* NFS Server for persistent storage
* Daily automated backup using cron job
* Backup format: `.tar.gz`
* Naming format example:

```
backup-YYYY-MM-DD.tar.gz
```

Backups must include:

* Website data
* Database logs
* Application logs

Ensure backup storage is secure and persistent.

---

# Question-5 – Monitoring 

To avoid downtime and production failures, the client wants complete monitoring.
You must implement infrastructure-level monitoring.

### 1. Infrastructure Monitoring (Metrics-Based Monitoring)
#### Tools to Configure (Metrics-Based Monitoring)

* `Prometheus` → Metrics Collector
* `Node Exporter` → System Metrics (CPU, RAM, Disk)
* `MySQL Exporter` → Database Metrics
* `Grafana` → Dashboard Visualization

You may import a pre-built dashboard.
Link: https://grafana.com/grafana/dashboards/

Your monitoring must show:

* CPU Usage
* Memory Usage
* Disk Usage
* MySQL Query Metrics

### 2. Application Monitoring (Log-Based Monitoring)
In production, logs are critical for debugging issues.
You must implement log-based monitoring.
#### Tools to Configure (Log-Based Monitoring)

* `Loki` → Log Collector
* `Promtail` → Log Extractor
* `Grafana` → Log Visualization

You must show logs for:

* WordPress Application Error Logs
* System Authentication Logs

Logs should be searchable from Grafana dashboard.

---
# How you will submit the assignment ???
## Create a repository 
* For submission of this assignment, you have to create your own GitHUB repostory account.
## What is name of the repository ??
* For clear visibility create the repository with following given example format.
* For example if candidate is `Ajay Sharma`, then he will create a respotiry named `ajay-sharma-assignment-repo`.

## Push the assignments 
* At the end push all your assignments to your repository.
