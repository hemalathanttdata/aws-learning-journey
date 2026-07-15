EC2(

**AWS Region**

**Definition**

**Region ante AWS data centers unna geographic location.**

Examples:

- Mumbai (ap-south-1)
- Hyderabad (ap-south-2)
- US East (us-east-1)

Region = City/Location

**Why We Use Region?**

✅ User ki daggara server create cheyyadaniki

✅ Latency reduce cheyyadaniki

✅ Data residency/compliance maintain cheyyadaniki

✅ Disaster Recovery kosam

Reason:

User daggara server unte

↓

Latency takkuva

↓

Application fast

**Availability Zone (AZ)**

**Definition**

**Availability Zone ante Region lopala unna separate AWS Data Center.**

Example:

Mumbai Region

|

|-- ap-south-1a

|-- ap-south-1b

|-- ap-south-1c

Availability Zone = Building/Data Center

Mumbai = Region

Building A = AZ-A

Building B = AZ-B

Building C = AZ-C

**Real-Time Example**

Only one server:

EC2

|

AZ-A

AZ-A fail ayithe:

❌ Website Down

EC2-1 → AZ-A

EC2-2 → AZ-B

AZ-A fail ayina:

✅ EC2-2 work chestundi

✅ Website continue avuthundi

#### **Region tells WHERE your server is located, and Availability Zone tells IN WHICH DATA CENTER inside that region your server is running.** 🚀

Multi-Region

\------------

Definition:

Deploying the same application in multiple AWS Regions.

Why?

\- Reduce Latency

\- Disaster Recovery

\- Global User Access

\- High Availability

When?

\- Global users

\- Business critical applications

\- Need for DR

Who Uses?

\- Amazon

\- Netflix

\- Microsoft

\- Google

Example:

India Users -> Mumbai Region

US Users -> Virginia Region

Europe Users -> London Region

**What is an Edge Location?**

**Answer:**

Edge Locations are AWS sites distributed globally and used by services such as CloudFront, Route 53, Global Accelerator, and AWS Shield to cache content and serve requests closer to end users, reducing latency and improving performance

Region = Big Hospital 🏥

Availability Zone = Building in Hospital 🏢

Edge Location = Local Clinic 🏪

Minor issue

↓

Nearby Clinic (Edge Location)

Major issue

↓

Main Hospital (Region)

\`\`

EC2 = Heart

VPC = Roads

Security Group = Security Guard

EBS = Hard Disk

IAM = Identity Card

Load Balancer = Traffic Police

CloudWatch = Doctor Monitoring Health

IAM → Permissions

VPC → Network

Security Group → Firewall

EBS → Storage

Load Balancer → Traffic Distribution

Auto Scaling → Scaling

CloudWatch → Monitoring  
<br/>

AWS(CLOUD COMPUTING)

**Cloud Service Models**

There are **3 types**:

IaaS → PaaS → SaaS

👉 Difference = **how much control you have**

**1\. IaaS (Infrastructure as a Service)**

👉 **You get virtual servers, storage, networking**  
👉 You manage everything else

What you handle: OS (Linux/Windows), Applications, Security settings

**🧩 Real-time example:**

👉 You rent a **house without furniture**

- You set everything yourself ✅

**. PaaS (Platform as a Service)**

**Cloud provides platform to run your app**  
👉 You only focus on application

**What you handle:**

- Only code (application)

**What cloud handles:**

- OS
- Servers
- Runtime

**Real-time example:**

👉 You rent a **fully furnished house**

- Just live, no setup needed ✅

**3\. SaaS (Software as a Service)**

👉 **Complete software available through internet**

👉 You just use it, no setup at all

**Examples:**

- Gmail
- Netflix
- Microsoft 365

**Real-time example:**

👉 Like staying in a **hotel**

- Everything ready ✅
- Just use it.

\`\`**pay as you go modeal------aws**