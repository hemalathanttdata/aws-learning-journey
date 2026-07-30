Lambda అంటే Server కాదు, ఒక Service.

✅ Runtime అంటే Code ని Run చేసే Environment.

✅ AWS Runtime ని Manage చేస్తుంది.

✅ Extra Libraries ని AWS Automatically Install చేయదు.

✅ Common Libraries కోసం **Lambda Layers** ఉపయోగిస్తాం.

**Why AWS introduced Lambda when EC2 already exists?**

EC2 లో Application Run చేయాలంటే Server Create చేసి, Operating System Maintain చేసి, 24/7 Instance Run చేయాలి. కానీ కొన్ని Applications రోజుకు కొన్ని Seconds లేదా Minutes మాత్రమే Run అవుతాయి. అలాంటి Event-driven Workloads కోసం EC2 Cost-effective కాదు. ఈ Problem ని Solve చేయడానికి AWS Lambda ని Introduce చేసింది. ఇందులో మనం Server Manage చేయాల్సిన అవసరం లేదు. Code మాత్రమే Upload చేస్తాం. Event వచ్చినప్పుడు AWS తన Infrastructure లో Execution Environment ని Automatically Provision చేసి Function ని Execute చేస్తుంది. Execution పూర్తయిన తర్వాత ఆ Environment ని Release చేస్తుంది. అందువల్ల Cost తగ్గుతుంది, Auto Scaling వస్తుంది, Infrastructure Management అవసరం ఉండదు.

**Q:** Lambda అంటే ఏమిటి?

AWS Lambda అనేది ఒక Serverless Compute Service. ఇందులో మనం Server ని Create చేయాల్సిన అవసరం లేదు. Code మాత్రమే Upload చేస్తాం. ఏదైనా Event వచ్చినప్పుడు Lambda Automatically Run అవుతుంది. Server Provisioning, Scaling, Patching, High Availability వంటి పనులన్నీ AWS Handle చేస్తుంది. DevOps లో దీనిని Automation, Event-driven Processing, Notifications, Log Processing, Scheduled Tasks వంటి వాటికి ఎక్కువగా ఉపయోగిస్తారు.

రోజుకు 3 seconds మాత్రమే Run అయ్యే పని కోసం 24 గంటలు EC2 Run చేయడం అంటే resources మరియు cost రెండూ waste. అలాంటి సందర్భంలో Lambda best choice.

**Lambda అంటే నిజంగా ఏమిటి?**

Lambda ఒక **Service**.

ఈ Service ఏమంటుంది?

**"నీ Code నాకు ఇవ్వు. ఎప్పుడు Run చేయాలో చెప్పు. మిగతా Server పని అంతా నేను చూసుకుంటాను."**

You

│

│ Upload Code

▼

Lambda Service

│

│ AWS keeps your code safely

▼

Waiting...

Event వచ్చే వరకు Wait చేస్తుంది.

**Event వచ్చింది**

ఉదాహరణకి

S3 లో File Upload అయింది.

File Upload

↓

Lambda

↓

AWS వెంటనే ఒక Server Ready చేస్తుంది

↓

నీ Code Run చేస్తుంది

↓

Output ఇస్తుంది

↓

Server ని Release చేస్తుంది

గమనించు...

Server **ఎప్పుడూ ఉండదని కాదు**.

**అవసరం వచ్చినప్పుడు AWS ఉపయోగిస్తుంది.**

పని అయిపోయాక ఆ Resources ని AWS మళ్లీ Free చేస్తుంది.

అందుకే నువ్వు Idle Server కి డబ్బు చెల్లించాల్సిన అవసరం ఉండదు.

**Before Lambda...**

Let's go back 10 years.

Suppose a company wants to execute a small Python program whenever a file is uploaded

How was this done before Lambda?

They had to launch an EC2 instance.

Even if the script runs for only **2 seconds**, the EC2 instance must remain running **24×7**.

That means:

- Pay for the server all day.
- Install the OS.
- Patch the OS.
- Update packages.
- Monitor CPU.
- Replace failed ins
- Imagine buying an entire bus just to carry one passenger once a day. 🚍
- That's inefficient.
- But the script runs only **5 seconds**.
- The server sits idle the remaining **86,395 seconds** of the day.
- That's a waste of money and resources.
- **AWS Thought**
- AWS engineers asked:
- "Why should customers manage servers just to run a few seconds of code?"
- Their solution was **AWS Lambda**.
- **Lambda అంటే?**
- చాలా Simple Definition.
- **Server గురించి ఆలోచించకుండా Code మాత్రమే Run చేయడానికి AWS ఇచ్చిన Service.**
- లేదంటే
- **Server ని AWS Manage చేస్తుంది.  
  Code ని మనం Manage చేస్తాం.**
- **Serverless అంటే ఏమిటి?**
- చాలామంది ఒక పెద్ద Mistake చేస్తారు.
- Serverless అంటే
- **Server ఉండదు**
- అనుకుంటారు.
- అది Wrong.
- Server ఉంటుంది.
- కానీ
- ఆ Server ని
- మనం చూడం.
- మనం Manage చేయం.
- AWS Manage చేస్తుంది.
- అందుకే దీనిని
- **Serverless Compute**

AWS Lambda ఎలా పనిచేస్తుంది?

Upload Code

↓

AWS Store చేస్తుంది

↓

Event కోసం Wait చేస్తుంది

↓

Event వచ్చింది

↓

Code Run చేస్తుంది

↓

Result ఇస్తుంది

↓

Stop అయిపోతుంది

గమనించు...

EC2 లాగా

24 Hours Running ఉండదు.

**Event అంటే ఏమిటి?**

Event అంటే

ఏదైనా ఒక పని జరగడం.

ఉదాహరణలు

✅ File Upload అయింది

✅ API Call వచ్చింది

✅ Time అయింది

✅ Message వచ్చింది

✅ Database లో Data వచ్చింది

అప్పుడు

Lambda వెంటనే Run అవుతుంది.

ఒక DevOps Engineer గా Lambda ని చాలా చోట్ల ఉపయోగిస్తారు.

**Example 1**

Night 10 PM

Unused EC2 Instances

↓

Automatically Stop

**Example 2**

Morning 8 AM

EC2

↓

Automatically Start

**ఇప్పుడు ఒక చిన్న Quiz 😄**

Suppose:

- S3 Bucket లో **1000 Files** ఒకేసారి Upload అయ్యాయి.

**Question:**

నీకు ఏమనిపిస్తోంది?

- Lambda ఒకే Server మీద అన్ని 1000 Files ని ఒక్కొక్కటిగా Process చేస్తుందా?
- లేక AWS చాలా Lambda Executions ని ఒకేసారి Run చేసి Parallel గా Process చేస్తుందా?
- **అసలు ఏమి జరుగుతుంది?**
- Suppose...
- S3 Bucket లో
- **1000 Images Upload అయ్యాయి.**
- image1.jpg
- image2.jpg
- image3.jpg
- ...
- image1000.jpg
- ప్రతి Upload ఒక **Event**.
- అంటే...
- 1000 Files అంటే...
- 👉 **1000 Events.**
- **AWS ఏమి చేస్తుంది?**
- AWS ఇలా ఆలోచిస్తుంది.
- "ఒక Lambda Function కోసం ఎందుకు Wait చేయాలి? నా దగ్గర చాల Servers ఉన్నాయి కదా!"
- అప్పుడు AWS...
- ఒక్క Lambda Execution కాదు...
- **1000 Lambda Executions** Start చేయగలదు.
- File1 ──► Lambda #1
- File2 ──► Lambda #2
- File3 ──► Lambda #3
- File4 ──► Lambda #4
- ...
- File1000 ──► Lambda #1000
- అన్నీ **ఒకేసారి (Parallel)** Run అవుతాయి.
- **ఒక Example**
- నీ School లో ఒక Teacher మాత్రమే ఉన్నారు అనుకో.
- 1000 Papers Correct చేయాలి.
- ఒక్క Teacher అయితే...
- Teacher
- ↓
- Paper1
- ↓
- Paper2
- ↓
- Paper3
- చాలా Time పడుతుంది.
- ఇప్పుడు...
- 1000 Teachers ఉన్నారు అనుకో.
- Teacher1 → Paper1
- Teacher2 → Paper2
- Teacher3 → Paper3
- ...
- Teacher1000 → Paper1000
- ఎంత Fast గా Complete అవుతుంది?
- 👉 చాలా త్వరగా.
- **AWS దగ్గర Servers తక్కువా?**
- లేదు.
- AWS దగ్గర ప్రపంచవ్యాప్తంగా వేలాది Servers ఉన్నాయి.
- అందుకే AWS అవసరమైతే చాలా Lambda Executions ని Parallel గా Run చేయగలదు.
- దీనినే **Auto Scaling** అంటారు.

**1000 Lambda అంటే 1000 కొత్త Servers Create అయ్యాయా?**

👉 **అవసరం లేదు.**

AWS తన Infrastructure లో ఉన్న Resources ని ఉపయోగించి, అవసరమైనంత Execution Environments ని Create చేస్తుంది. నీకు అవి ఎలా Allocate అయ్యాయో కనిపించదు. నీకు కనిపించేది ఒక్కటే:

- Event వచ్చింది.
- Lambda Run అయింది.
- Result వచ్చింది.
- **Runtime అంటే ఏమిటి?**
- చాలా Simple Definition.
- **Runtime అంటే నీ Code ని Run చేయడానికి అవసరమైన Environment.**
- అంటే...
- Python Code అయితే...
- Python Install అయి ఉండాలి.
- Java Code అయితే...
- JVM ఉండాలి.
- **Runtime అంటే Code ని Run చేయడానికి అవసరమైన Environment.**
- ✅ **Runtime ని AWS Manage చేస్తుంది.**

**ఇప్పుడు ఒక చాలా Important Question ❓**

నువ్వు Lambda Function Upload చేశావు.

ఆ Function లో ఇలా ఉంది:

print("Hello")

**కానీ ఇందులో Python Library (requests) కూడా use చేశావు.**

అప్పుడు...

ఆ Library ఎవరు Install చేస్తారు?

- AWS Automatically Install చేస్తుందా?
- లేక మనమే Upload చేయాలా?

👉

**AWS ఏమి ఇస్తుంది?**

AWS Lambda Runtime లో కొన్ని Basic Libraries మాత్రమే ఉంటాయి.

ఉదాహరణకు Python Runtime లో:

- Python Interpreter ✅
- Standard Python Libraries ✅

మరియు AWS SDK అయిన **boto3** కూడా సాధారణంగా ముందే ఉంటుంది.

AWS ఇలా అంటుంది:

"ఈ Library నా Runtime లో లేదు."

అప్పుడు ఏమవుతుంది?

ImportError

లేదా

No module named 'requests'

అనే Error వస్తుంది.

**మరి Libraries ఎలా ఇస్తాం?**

రెండు Methods ఉన్నాయి.

**Method 1 (Simple)**

Library ని Install చేసి,

Code తో పాటు ZIP చేసి Upload చేస్తాం.

MyProject/

├── lambda_function.py

├── requests/

├── urllib3/

├── certifi/

అన్నీ ZIP చేసి Upload.

**Method 2 (Professional - DevOps లో ఎక్కువగా Use చేస్తారు)**

**Lambda Layers**

Lambda Function

│

▼

Lambda Layer

│

▼

requests

pandas

numpy

ఒక Layer ని చాలా Lambda Functions Share చేసుకోవచ్చు.

ఇది Professional Way.

**ఇప్పుడు ఒక Question అడుగుతాను. 😊**

Suppose...

నీ Lambda Function కి **pandas** Library అవసరం ఉంది.

ఇప్పుడు నువ్వు ఏది Choose చేస్తావు?

**Option A:** ప్రతి Lambda Function తో pandas ని ZIP చేసి Upload చేస్తావా?

**Option B:** ఒక Lambda Layer Create చేసి, అన్ని Lambda Functions దానిని Use చేసేలా చేస్తావా?

ఒక Lambda Layer Create చేసి, అన్ని Lambda Functions దానిని Use chasth

**Real-Time DevOps Example**

మన Project లో 50 Lambda Functions ఉన్నాయి.

అన్నీ AWS Services ని Access చేయడానికి Common Utility Code Use చేస్తున్నాయి.

ఉదాహరణకు:

- Database Connection
- Logging Functions
- Common Validation
- Helper Functions

ఇవి ప్రతి Lambda లో Copy-Paste చేయడం కంటే...

ఒక **Lambda Layer** లో పెట్టి అన్ని Functions కి Attach చేస్తారు.

**Layer అంటే Code Store చేసే Place."**

❌ పూర్తిగా కాదు.

**Layer అనేది ప్రధానంగా Common Dependencies, Libraries లేదా Shared Code ని Reuse చేయడానికి ఉపయోగించే Feature.**

**ఇప్పటివరకు మనం నేర్చుకున్నవి**

✅ Lambda అంటే Server కాదు, ఒక Service.

✅ Runtime అంటే Code ని Run చేసే Environment.

✅ AWS Runtime ని Manage చేస్తుంది.

✅ Extra Libraries ని AWS Automatically Install చేయదు.

✅ Common Libraries కోసం **Lambda Layers** ఉపయోగిస్తాం.

Event vachinappudu Lambda automatically server ni create chestundi.

🟡 **ఇక్కడ చిన్న correction.**

ఇలా చెప్పడం కంటే ఇలా చెప్పడం ఇంకా correct:

**Event వచ్చినప్పుడు AWS Lambda, AWS infrastructure లో already available ఉన్న compute resources ని use చేసి ఒక execution environment ని start చేస్తుంది.**

ఎందుకంటే...

AWS ప్రతిసారి ఒక కొత్త Physical Server కొనదు లేదా Build చేయదు. 😄

AWS Data Centers లో ఇప్పటికే చాలా Servers ఉంటాయి.

వాటిలో ఒక execution environment ని నీ function కోసం ఉపయోగిస్తుంది.

**Next:**

1️⃣ Lambda Architecture  
2️⃣ Lambda Function Creation (Console Hands-on)  
3️⃣ Handler, Event, Context  
4️⃣ S3 Trigger Project  
5️⃣ IAM Permissions  
6️⃣ CloudWatch Logs  
7️⃣ VPC Integration  
8️⃣ CI/CD Deployment

**Environment Variables ఎందుకు ఉపయోగిస్తారు?**

**Answer:**

Environment Variables అనేవి Configuration Values ని Code కి బయట Store చేయడానికి ఉపయోగిస్తారు. దీనివల్ల Sensitive Information (Passwords, API Keys), Environment-specific Values (Dev, QA, Production URLs) ని Code మార్చకుండా Manage చేయవచ్చు. ఇది Security, Reusability, Maintainability ని Improve చేస్తుంది.

\--------------------------TASK-------------------------

Lmabda+EventBridge+ec2+s3 cleanup automation???

Step1: IAM ROLE CREATE

Step2:ec2 and s3 setup

Step3:lamda create

Step4:lambda code

Step5:test lambda

Eventbridge schedule

COMPLETED TOPICS::

Lambda function

Iam permissions

Ec2tag-based cleanup

S3 object cleanup

Cloudwatch logs

envtbridge scheduled execution

lambda error handling

sns email notification after cleanup

cloudwath monitoring &alarms

task::

**Lmabda Error handling+SNS notification**

Suppose every day 11:50 pm ki cleanup lambda run ayyindi.

Manaki email notification ravali..

Cleanup completed successfully

If any error vachina::cleanup failed

Steps::

| ✅ Trigger Lambda manually (Test Event) | ✅ Completed |
| --------------------------------------- | ------------ |

| ✅ Upload a ZIP package | ⏳ Not yet (మనం Console Inline Editor use చేశాం) |
| ----------------------- | ------------------------------------------------ |

| ✅ Create an IAM execution role | ✅ Completed |
| ------------------------------- | ------------ |

| ✅ Trigger Lambda from S3 | ⏳ Pending |
| ------------------------- | ---------- |

| ✅ Trigger Lambda using EventBridge | ✅ Completed |
| ----------------------------------- | ------------ |

| ✅ Send SNS notifications using Lambda | ✅ Completed (IAM permission issue కూడా troubleshoot చేశాం) |
| -------------------------------------- | ----------------------------------------------------------- |

| ✅ Read messages from SQS | ❌ Pending |
| ------------------------- | ---------- |

| ✅ Create and use Lambda Layers | 🟡 Theory Completed, Hands-on Pending |
| ------------------------------- | ------------------------------------- |

| ✅ Configure Environment Variables | 🟡 Theory Completed, Hands-on Pending |
| ---------------------------------- | ------------------------------------- |

| ✅ Publish Versions and create Aliases | ❌ Pending |
| -------------------------------------- | ---------- |

| ✅ View logs in CloudWatch | ✅ Completed |
| -------------------------- | ------------ |

| ✅ Connect Lambda to a VPC | ❌ Pending |
| -------------------------- | ---------- |

| ✅ Test Timeout and Memory settings | ❌ Pending |
| ----------------------------------- | ---------- |

\---------------------+++++++++++++++++++++\_**\_**\_**\_**\_**\_**\_**\_**\__

| ✅ Upload a ZIP package | ⏳ Not yet (మనం Console Inline Editor use చేశాం) |
| ----------------------- | ------------------------------------------------ |

**Q: Why do we upload a ZIP package instead of writing code in the Lambda console?**

**Answer:**

In real-world projects, Lambda functions usually consist of multiple Python files, helper modules, configuration files, and dependencies. Managing such code in the AWS Console is difficult. Therefore, developers build the project locally, test it, package it as a ZIP file, and deploy it to Lambda. This makes deployment easier, supports version control, and integrates well with CI/CD pipelines.

Steps:

| ✅ Trigger Lambda from S3 | ⏳ Pending |
| ------------------------- | ---------- |

**How does Lambda know when to execute after a file is uploaded to S3?**

**Answer:**

Amazon S3 generates an Object Created event whenever a new object is uploaded. This event is configured as a trigger for the Lambda function. S3 invokes the Lambda function asynchronously and passes the event payload containing details such as the bucket name, object key, event type, and timestamp.

| ✅ Trigger Lambda using EventBridge | ✅ Completed |
| ----------------------------------- | ------------ |

**"EventBridge ను Time-based Scheduling కోసం ఉపయోగిస్తాం. నిర్ణయించిన Time కి Lambda Function ని Automatically Trigger చేస్తుంది."** ✅

**EventBridge → Lambda (Simple Steps to Remember)**

- **Go to EventBridge**
- **Create Rule**
- **Give Rule Name**
- **Select Schedule**
- **Enter Cron/Rate Expression** (Example: Every day 11 PM)
- **Target → Select Lambda Function**
- **Choose Your Lambda**
- **Create Rule**
- **Wait for Schedule** (or trigger manually if testing)

| ✅ Read messages from SQS | ❌ Pending |
| ------------------------- | ---------- |

**SQS ఉపయోగించేది, ఒకేసారి చాలా Requests వచ్చినప్పుడు వాటిని Queue లో పెట్టి, Lambda ఒక్కొక్కటిగా లేదా Batch లుగా Process చేయడానికి.** ✅

**Real-time Example**

Amazon లో **10,000 Orders** ఒకేసారి వచ్చాయి.

❌ వెంటనే Database కి పంపితే Server Down అయ్యే అవకాశం ఉంది.

అప్పుడు:

Orders

↓

SQS Queue

↓

Lambda

↓

Database

అంటే **SQS ఒక Waiting Line (Queue)** లాగా పనిచేస్తుంది.

**SQS Queue లో Messages ని తాత్కాలికంగా Store చేస్తుంది. Lambda ఆ Queue నుండి Messages ని Read చేసి Process చేస్తుంది."** ✅

| ✅ Create and use Lambda Layers | 🟡 Theory Completed, Hands-on Pending |
| ------------------------------- | ------------------------------------- |

**అన్ని Lambda Functions లో Common Libraries లేదా Common Code ని మళ్లీ మళ్లీ Copy చేయకుండా, ఒక్కచోట Store చేసి అన్ని Functions Use చేయడానికి Lambda Layers ఉపయోగిస్తాం.** ✅

**Real-Time Example**

మన దగ్గర 20 Lambda Functions ఉన్నాయి.

అన్నింటికీ pandas Library కావాలి.

❌ ప్రతి Lambda లో pandas Upload చేస్తామా?

లేదు.

**Simple Steps (Remember)**

- Create Layer
- Upload ZIP (Library/Common Code)
- Create Layer Version
- Open Lambda
- Add Layer
- Deploy
- Lambda uses the Layer

**"Lambda Layers ను Common Libraries మరియు Shared Code ని Reuse చేయడానికి ఉపయోగిస్తాం. దీనివల్ల Duplicate Code తగ్గుతుంది, Maintenance సులభం అవుతుంది."** ✅

**గుర్తుంచుకో**

- **ZIP Deployment** = నీ Lambda Function Code ని Upload చేస్తుంది.
- **Lambda Layer** = చాలామంది Lambda Functions కలిసి Use చేసే Common Libraries/Code ని Upload చేస్తుంది.

**ZIP = Main Code** 📦

**Layer = Common Libraries** 📚

| ✅ Configure Environment Variables | 🟡 Theory Completed, Hands-on Pending |
| ---------------------------------- | ------------------------------------- |

**Password, API Key, Database URL, Bucket Name వంటి Configuration Values ని Code లో కాకుండా బయట Secure గా Store చేయడానికి Environment Variables ఉపయోగిస్తాం.** ✅

❌ **Bad Practice**

password = "Welcome@123"

✅ **Good Practice**

password = os.environ\["DB_PASSWORD"\]

**Simple Steps (Remember)**

- Open Lambda
- Configuration
- Environment Variables
- Add Key & Value
- Save
- Read in Python using os.environ

Environment Variables ను Sensitive Information మరియు Configuration Values ని Code బయట Store చేసి, Code మార్చకుండా Manage చేయడానికి ఉపయోగిస్తాం."

| ✅ Publish Versions and create Aliases | ❌ Pending |
| -------------------------------------- | ---------- |

**Interview One-liner**

**"Versions ను Lambda code snapshots కోసం, Aliases ను ఆ Versions ని easy గా switch చేయడానికి ఉపయోగిస్తాం."** ✅

**గుర్తుంచుకో**

- 📌 **Version = Snapshot of your Lambda code.**
- 🏷️ **Alias = Friendly name (PROD, DEV, TEST) pointing to a Version.**

**Simple Steps (Remember)**

- Update Lambda Code
- Publish Version
- Create Alias
- Point Alias to Version
- Use Alias instead of Version Number
- **Alias అంటే?**
- Alias = **Nickname**
- **One-line Use**
- 👉 **Lambda Code కి Stable Versions create చేసి, వాటిని Easy గా Manage చేయడానికి Versions & Aliases ఉపయోగిస్తాం.** ✅

<div class="joplin-table-wrapper"><table><tbody><tr><th><p>✅ Connect Lambda to a VPC</p></th><th><p>❌ Pending</p></th></tr><tr><td><p><strong>"VPC Connection = Lambda కి Private Network లోకి Entry Pass ఇవ్వడం."</strong></p><p><strong>గుర్తుంచుకో</strong></p><ul><li>🌐 <strong>Without VPC</strong> → Lambda Public AWS Services (S3, SNS, SQS, EventBridge) ని సులభంగా Access చేయగలదు.</li><li>🔒 <strong>With VPC</strong> → Lambda Private Resources (RDS, Private EC2, ElastiCache) ని కూడా Access చేయగలదు.</li></ul><p><strong>Simple Steps (Remember)</strong></p><ol><li>Create VPC</li><li>Create Private Subnet</li><li>Create Security Group</li><li>Open Lambda</li><li>Configuration → VPC</li><li>Select VPC</li><li>Select Private Subnets</li><li>Select Security Group</li><li>Save</li></ol><p>✅ Test Timeout and Memory settings ❌ Pending</p><p><strong>Lambda కి ఎంత RAM (Memory) ఇవ్వాలి, ఎంత Time వరకు Run అవ్వాలి (Timeout) అనేది Configuration చేయడానికి Memory &amp; Timeout Settings ఉపయోగిస్తాం.</strong> ✅<strong>Memory అంటే?</strong></p><p>👉 <strong>Lambda కి పని చేయడానికి ఎంత RAM ఇవ్వాలో.</strong></p><p><strong>Timeout అంటే?</strong></p><p>👉 <strong>Lambda ఎంత సేపు Run అవ్వాలో Limit పెట్టడం.</strong></p><p>Example:</p><p>30 Seconds</p><p>30 seconds దాటితే AWS Lambda ని Stop చేస్తుంది.</p><p><strong>Simple Steps (Remember)</strong></p><ol><li>Open Lambda</li><li>Configuration</li><li>General Configuration</li><li>Edit</li><li>Change Memory</li><li>Change Timeout</li><li>Save</li></ol><p><strong>Memory performance ని, Timeout maximum execution time ని control చేయడానికి ఈ settings ఉపయోగిస్తాం."</strong> ✅</p><p><strong>గుర్తుంచుకో</strong></p><ul><li>🧠 <strong>Memory = ఎంత శక్తితో పని చేయాలి.</strong></li><li>⏱️ <strong>Timeout = ఎంత సేపు పని చే</strong></li></ul><p><strong>DevOps Engineer కి Lambda లో ఇంకా ఏమి అవసరం?</strong></p><p>కొన్ని advanced topics మాత్రమే మిగిలి ఉంటాయి:</p><ul><li>CI/CD ద్వారా Lambda Deployment (Jenkins / GitHub Actions)</li><li>Infrastructure as Code (Terraform / CloudFormation) ద్వారా Lambda Create చేయడం</li><li>Monitoring &amp; Alerting (CloudWatch Alarms)</li><li>X-Ray Tracing (Performance Debugging)</li><li>Provisioned Concurrency (Advanced Performance Optimization)</li></ul></td><td></td></tr></tbody></table></div>