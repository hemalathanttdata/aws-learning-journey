AWS and DEVOPS

What is devops?  
DevOps is a culture + tools + process to deliver software faster and with fewer errors.

DevOps = Development (Dev) + Operations (Ops)

It is a **way of working** where:

- Developers (who write code)
- Operations team (who deploy & manage servers)

**work together instead of separately**

DevOps is a process that helps build, test, and release software faster and more reliably.

**Before DevOps:** Developers and operations worked separately, causing slow releases and frequent issues.

main issues before DevOps::

**1\. Slow releases**

- Code took weeks/months to go live

👉 **2\. Miscommunication**

- Dev and Ops worked separately → misunderstandings

👉 **3\. Deployment failures**

- "It works on my machine" but fails in production

👉 **4\. Manual work**

- Everything done manually → more errors

👉 **5\. Bug fixing very slow**

- Issues found late and took long to fix

👉 **6\. No automation**

- Testing & deployment not automated

👉 **7\. Blame game culture**

- Dev blames Ops, Ops blames Dev

👉 **8\. Unstable environments**

- Dev, test, production different → unexpected issues

✅ **In short:**  
👉 _Before DevOps → slow, error-prone, and disconnected workflow._

**How DevOps solves old issues**

👉 **1\. Slow releases → Faster delivery**

- Uses automation + CI/CD → code goes live quickly

👉 **2\. Miscommunication → Better collaboration**

- Dev & Ops work together in one team

👉 **3\. Deployment failures → Reliable deployments**

- Automated testing catches errors early

👉 **4\. Manual work → Automation**

- Build, test, deploy all automated

👉 **5\. Slow bug fixing → Quick feedback**

- Monitoring tools detect issues immediately

👉 **6\. No automation → CI/CD pipelines**

- Continuous integration & deployment

👉 **7\. Blame game → Shared responsibility**

- One team owns the product end-to-end

👉 **8\. Unstable environments → Consistency**

- Same setup using containers (Docker) & scripts

**🧠 One-line summary**

👉 **DevOps solves problems using automation, collaboration, and continuous delivery.**

/////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////

Before DevOps,

- **Waterfall Model** (Most common)

2\. **Agile (early phase before DevOps integration)**

**1\. Waterfall Model (Most common)**

👉 Work happens step-by-step like a flow:

- Requirement
- Design
- Development
- Testing
- Deployment

❌ Problem:

- Very slow
- No going back easily
- Testing happens at the end

**2\. Agile (early phase before DevOps integration)**

👉 Work is divided into small parts (sprints)

✔ Faster than Waterfall  
✔ Frequent releases

❌ Still:

- Dev and Ops not fully connected
- Deployment still manual

**⚡ Simple Comparison**

👉 **Waterfall** → slow & rigid  
👉 **Agile (without DevOps)** → faster but deployment pain  
👉 **DevOps** → fast + automated + smooth delivery

**🧠 One-line answer**

👉 **Before DevOps, teams mainly used Waterfall and early Agile methods, where development and operations worked separately.**

Why Waterfall failed??

**1\. No flexibility**

- Once a phase is done, you **cannot go back easily**
- If the client wants changes → big problem  
   💡 Real issue: requirements change in real projects

**2\. Late testing**

- Testing happens **only at the end**
- Bugs are found very late  
   💥 Fixing them becomes costly and time-consuming

**3\. Slow delivery**

- Entire project must finish before release
- Customer waits a long time to see results

**4\. Poor customer involvement**

- Client is involved only at start & end
- Final product may not meet expectations

**5\. High risk**

- If something goes wrong → entire project is affected
- No early feedback to correct mistakes

**6\. "All or nothing" approach**

- Full system is delivered at once
- If it fails → everything fails ❌
- **Simple summary**
- 👉 **Waterfall failed because it is rigid, slow, and doesn't handle change or feedback well.**

\>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>

**What is Agile Methodology?**

👉 **Agile means developing software in small parts, with continuous feedback and improvements.**

**How Agile works (simple steps)**

Instead of building everything at once:

- Break project into **small features**
- Work in short cycles called **sprints** (1-2 weeks)
- In each sprint:
  - Develop ✅
  - Test ✅
  - Show to client ✅
- Get feedback and improve
- Repeat this process again and again
- 👉 **Don't build everything at once - build little by little and improve continuously**

**👉 In Waterfall:**

- Build full app (login, cart, payment) → deliver after months ❌

**👉 In Agile:**

- Sprint 1 → Login page
- Sprint 2 → Product page
- Sprint 3 → Cart

✅ After each sprint:

- Client checks
- Gives feedback
- You improve immediately
- 👉 **Agile is a method where software is built step-by-step with continuous feedback and quick delivery.**

**In Agile**

👉 Development is **fast and flexible**  
❌ But **deployment is mostly manual**

- Dev team finishes sprint ✅
- Then Ops team manually deploys ❌
- This causes:
  - Delays
  - Errors
  - Dependency on ops team
- Agile has manual deployment limitations, and DevOps solves it by automating deployment and improving collaboration

👉 **DevOps comes to solve this exact problem**

It adds:

**✅ Automation**

- No manual deployment …Everything is automated
- **What is a Pipeline in DevOps?**
- 👉 **Pipeline = a series of automated steps that take your code from developer → production**
- Instead of doing things manually,  
   **everything happens automatically step by step**
- Pipeline Flow
- Code → Build → Test → Deploy
- Without Pipeline ❌

**Without Pipeline ❌**

- You build manually
- You test manually
- You deploy manually  
   👉 Slow + errors
- **With Pipeline ✅**
- You push code to GitHub
- Pipeline starts automatically 🔄
- Build code ✅
- Run tests ✅
- If everything is OK →
- Automatically deploy to server (AWS) 🚀
- 👉 No manual work!

\>>>>>A pipeline is an automated process that moves code from development to deployment step by step

|||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||  
SDLC:

Plan-Requirement Gathering-Analysis-Design-code(development)-Test-Release-Monitoring

SDLC = step-by-step process used to build software in an organized way

**How SDLC works in real life**

**🧩 Example: Building a Banking App**

👉 **1\. Requirement**

- Bank says: "We need login + money transfer"

👉 **2\. Design**

- UI design + system design prepared

👉 **3\. Development**

- Developers write code

👉 **4\. Testing**

- Test login, transfer, security

👉 **5\. Deployment**

- App released to users

👉 **6\. Maintenance**

- Fix bugs, add new features

High-Level Design (HLD)

**Big picture of the system**

- Shows overall architecture
- How components are connected
- Technology choice

**📌 Example (Banking App)**

- Use **Frontend + Backend + Database**
- Backend connects to database
- Use AWS cloud

👉 It answers:  
**"What are we building and how major parts connect?"**

**✅ Low-Level Design (LLD)**

👉 **Detailed internal design**

- How each component works internally
- Database tables, APIs, logic
- Small details

**📌 Example (Banking App)**

- Login API structure
- Database table: Users (name, password)
- Validation logic

👉 It answers:  
**"How exactly will each part work?"**

|||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||

**CLOUD(AWS)**

**Cloud = using computers, storage, and services over the internet instead of your own local machines.**

**Server is like the kitchen that prepares and serves orders.**

**Cloud is like renting a fully managed kitchen instead of building and maintaining your own kitchen.**

** Server = Kitchen**

** Cloud = Kitchen infrastructure rent service (AWS/Azure/GCP)**

** Client = Customer**

** Internet = Waiter**

**Instead of buying servers,  
you rent resources online (AWS, Azure, etc.)**

**Real-life example**

**👉 Like electricity ⚡**

- **You don't build power plant**
- **You just use electricity and pay bill**

**👉 Same:**

- **You don't buy servers**
- **You use AWS and pay for usage**

**Why Cloud is Required?**

**1\. No need to buy hardware,,** **Scalability ,,** **Pay only for usage,** **Fast setup**

**Before Cloud, what was used?**

**👉 On-Premises Infrastructure**

**🏢 What is On-Premise?**

- **Companies buy:**
  - **Physical servers**
  - **Data centers**
  - **Networking equipment**

**🧩 Real Example (Before Cloud)**

**👉 A company wants to build a website:**

- **Buy servers 🖥️**
- **Set up data center 🏢**
- **Hire people to manage**
- **If traffic increases:**
  - **Need to buy more servers (takes weeks)**

**👉 Before Cloud**

- **Companies managed everything → costly, slow**

**👉 After Cloud** **Like using public bus 🚌**

**Just use services → fast, scalable, easy**

**Types of Cloud**

**There are 3 main types:**

- **Public Cloud**

**Cloud provided by third-party companies like:**

- **AWS**
- **Azure**
- **Google Cloud**
- Anyone can use it over the internet
- Like using **public bus** 🚌

- **Private Cloud::** **Cloud used by only one company**
-  A bank creates its own cloud inside company
-  Sensitive data stays inside
- Like **your own car** 🚗
- **Hybrid Cloud::** **Combination of Public + Private Cloud**
-  Bank stores sensitive data → Private Cloud
-  Runs website → Public Cloud

Like **using bike + bus together** 🏍️🚌

- Choose based on need

\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\

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

. PaaS (Platform as a Service)

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
- Just use i

||||||||||||||||||||||||||||||

What is a Server?

**Server = a computer that serves requests**

**Real-time Example**

**🌍 Example: Opening a Website**

- You open Google on your phone 📱
- Your phone sends request → server
- Server sends back website data ✅

👉 That system which responds = **Server**

**Client vs Server**

- **Client** → Your mobile/laptop
- **Server** → Powerful machine storing data

**Easy Daily Example**

👉 Think like a **restaurant** 🍽️

- You (client) → order food
- Kitchen (server) → prepares & gives food

**Types of Servers**

- 🌐 Web Server → Hosts websites
- 📂 File Server → Stores files
- 🗄️ Database Server → Stores data
- **🎯 Final Understanding**
- 👉 **Server = a computer that receives requests and sends responses over a network**
- **🧠 One-line answer**
- 👉 **A server is a system that provides data or services to other systems over the internet or a network.**

**🖥️ Physical Server**

👉 **Real, actual hardware machine**

**✅ Features**

- Tangible (you can touch it)
- Kept in data centers
- One machine = one system

**🧩 Example**

👉 Big server room in a company 🏢

- Each server is a large computer

**Virtual Server**

👉 **Software-based server running on physical hardware**

👉 One physical server → multiple virtual servers

**✅ Features**

- Created using software (hypervisor)
- Can create/delete in minutes
- Cost-effective
- Scalable

**🧩 Example**

👉 AWS EC2 instance

- Not physical, but behaves like real computer

**🧠 Easy Real-life Comparison**

👉 **Physical Server** = Independent house 🏠  
👉 **Virtual Server** = Apartments in one building 🏢

- One building → many flats
- One hardware → many virtual servers

||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||

**"What is virtualization & hypervisor?"**

**👉 Virtualization = creating multiple virtual servers from one physical server using software**

**👉 One real computer → behaves like many computers**

**You have 1 powerful server  
Using virtualization, you create:**

- **5 virtual machines (VMs)**
- **Each acts like independent server ✅**
- **What is Hypervisor?**
- 👉 **Hypervisor = software that creates and manages virtual machines**

**🧠 Simple meaning**

**👉 It is the manager between:**

- **Physical server (hardware)**
- **Virtual machines**
- Physical Server (Hardware) ↓ Hypervisor ↓ Virtual Machines (VM1, VM2, VM3...)

**Role of Hypervisor**

- **Creates virtual servers**
- **Allocates CPU, RAM, storage**
- **Keeps VMs isolated**

**Real-time Example (AWS)**

**👉 AWS EC2 uses virtualization**

- **AWS has huge physical servers**
- **Hypervisor creates multiple EC2 instances**
- **You launch one VM → your own server ✅**

**Easy Real-life Example**

**👉 Think of a school building 🏫**

- **Building = Physical server**
- **Classrooms = Virtual machines**
- **Principal = Hypervisor (controls everything)**

**🧠 One-line answer**

**👉 Virtualization is the creation of virtual machines from a single physical system, and a hypervisor is the software that manages those virtual machines.**