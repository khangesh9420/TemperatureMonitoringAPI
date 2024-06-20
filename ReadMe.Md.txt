The Diagram is to planning for creating the Temperature monitoring API, and this is the following a block digram that how the API will work.





+-----------------------------------+
|           Client Side             |
|      (Web Dashboard - React)      |
|                                   |
| +-------------------------------+ |
| | 1. User Requests Data         | |
| | 2. Displays Real-Time Data    | |
| | 3. Visualization & Alerts     | |
| +-------------------------------+ |
+--------------------+--------------+
                     |
                     |
                     v
+--------------------+--------------+
|           Server Side             |
|    (RESTful API - C# & ASP.NET)   |
|                                   |
| +-------------------------------+ |
| | 1. API Requests Data from     | |
| |    Public API                 | |
| | 2. Processes Data             | |
| | 3. Stores Data in Database    | |
| | 4. Serves Data to Dashboard   | |
| +-------------------------------+ |
+--------------------+--------------+
                     |
                     |
                     v
+--------------------+--------------+            +----------------------+
|    Data Source (Public API)       |<---------->|    Public API        |
|       (e.g., OpenWeatherMap)      |            |  (Temperature Data)  |
|                                   |            +----------------------+
| +-------------------------------+ |
| | 1. Provides Real-Time          | |
| |    Temperature Data            | |
| +-------------------------------+ |
+--------------------+--------------+
                     |
                     |
                     v
+--------------------+--------------+
|           Database                 |
|  (SQL Server or PostgreSQL)        |
|                                    |
| +-------------------------------+  |
| | 1. Stores Processed Data      |  |
| | 2. Provides Data for Analysis |  |
| +-------------------------------+  |
+--------------------+--------------+
                     |
                     |
                     v
+--------------------+--------------+
|  Infrastructure Provisioning       |
|      (Terraform)                   |
|                                    |
| +-------------------------------+  |
| | 1. Provisions Cloud Resources |  |
| +-------------------------------+  |
+--------------------+--------------+
                     |
                     |
                     v
+--------------------+--------------+
|   Configuration Management        |
|        (Ansible)                  |
|                                    |
| +-------------------------------+  |
| | 1. Configures Environments    |  |
| | 2. Deploys Applications       |  |
| +-------------------------------+  |
+--------------------+--------------+
                     |
                     |
                     v
+--------------------+--------------+
|    Continuous Integration &        |
|    Continuous Deployment (CI/CD)   |
|           (GitLab)                 |
|                                    |
| +-------------------------------+  |
| | 1. Code Repository            |  |
| | 2. Pipeline Automation        |  |
| | 3. Builds and Tests           |  |
| | 4. Deploys via Ansible        |  |
| +-------------------------------+  |
+--------------------+--------------+
                     |
                     |
                     v
+--------------------+--------------+            +----------------------+
|  Code Quality & Security Analysis  |<---------->|    SonarQube         |
|          (SonarQube)               |            |  (Code Analysis)    |
|                                    |            +----------------------+
| +-------------------------------+  |
| | 1. Analyzes Code Quality      |  |
| | 2. Checks Security            |  |
| | 3. Reports Issues             |  |
| +-------------------------------+  |
+--------------------+--------------+
                     |
                     |
                     v
+--------------------+--------------+
|  Containerization & Orchestration  |
|  (Docker & Kubernetes)             |
|                                    |
| +-------------------------------+  |
| | 1. Containerizes Applications |  |
| | 2. Orchestrates Deployments   |  |
| +-------------------------------+  |
+-----------------------------------+
