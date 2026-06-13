# Lab - Agent Studio Use Case: AI Customer Retention (Telecom)

In this lab, you will explore Cloudera Agent Studio to deploy an AI-driven Customer Retention application for a Telecom use case. 

**Use Case Scenario:** AI Customer Retention delivers hyper-personalized telecom experiences using AI Agents that analyze customer profiles and usage behavior, predict churn risk, review competitor offers, and recommend the right plans, add-ons, or loyalty benefits — all in real-time on Cloudera AI.

**Objective:** Stay ahead in a competitive telecom market by leveraging AI agents that continuously monitor customer activity and market dynamics — transforming customer experience and driving proactive retention strategies.

**Business Impact:**

* **Enhanced Customer Loyalty & Engagement:** AI-powered personalization increases satisfaction and reduces churn by offering timely upgrades, rewards, and retention incentives tailored to each user.
  
* **Boosted Revenue via Upsell & Cross-sell:** Real-time usage insights empower agents to recommend data boosters, family plans, roaming packs, and OTT bundles — maximizing revenue per user.
  
* **Competitive Edge through Market Intelligence:** Continuous analysis of competitor promotions enables SmartTel to respond instantly with attractive offers and localized pricing advantages.
  
* **Operational Efficiency & Regulatory Alignment:** Automated, auditable decision-making minimizes manual workloads, enhances campaign ROI, and ensures alignment with data privacy and regional telecom regulations.
  

![Telecom Agentic Workflow Architecture](telecom_workflow_architecture_diagram.png)

## Requirements

Ensure the following requirements and credentials are met in order to run this exercise (these will be shared by the Trainers):

- [ ] Workload User and Password from User Profile
      
- [ ] Virtual Warehouse Name from CDW Impala host (provided below)
      
- [ ] Database Name from CDW Impala (`default_database`)
      

---

## Tasks

### Step 1: Log in to Cloudera Platform & AI Workbench

1. From the Cloudera on cloud Tenant home page, click on Machine Learning.

![Cloudera on Cloud Tenant Home](cloudera_on_cloud_tenant_home.png)

2. The Cloudera AI Home shows all available Workbenches, which is a compute resource allocation for Data Science related jobs.

Click on the `{{ (cai_workbench_name) | default("only")}}` Workbench that appears.

3. Go to **Projects** on the left side panel > Select **Public Projects** from the dropdown.
4. Click on the publicly available project named **AgentiAI**.
   
   ![Select Public Project HOL_Agent_Studio](cai_select_public_project.png)

5. Click on **AI Studios** > **Agent Studio**.
   
   ![Open Agent Studio from Left Menu](cai_open_agent_studio.png)

### Step 2: Understand the Agent Studio Environment

Take a moment to understand the main components of the Agent Studio interface:

1. **Agentic Workflows:** Dashboard with End-to-End Agentic Workflows & Use Cases Development and Deployment.
   
2. **Tools Catalog:** Build custom Python tools to enhance your AI agents capabilities and supercharge your workflows.
   
3. **LLMs:** Hybrid Muti LLM Model Registry to Register language models which will be used to build agents and workflows.
  
4. **Deployed Workflows:** Single Pane of Glass to All Production Workflow and Use Cases.
   
5. **Draft Workflows:** Management and Collaboration all the Development Workflows.
    
6. **Workflow Templates:** Workflows Catalog to share and re-use the workflows.
    
7. **Create:** Build your Agentic Workflow from scratch.
    

   ![Agent Studio Environment Overview](agent_studio_dashboard_overview.png)


### Step 3: Building the Use Case Workflow

1. Click **Create** > Select the Workflow from the **AI Customer Retention Template**.
   
2. Name the use case: **Userxxx - AI Customer Retention** (replace `Userxxx` with your assigned user).
   
   ![Select AI Customer Retention Template](select_telco_template.png)

4. **Understand the Workflow and Agents:**
   
   * Click **Edit Agents** to understand the functionality of each agent and the flow (Name, Role, Backstory, Goal).
     
   * ⚠️ **Don’t Make Any Changes but Just Close.**
     
   * Click **Save & Next** until you arrive at the **Configure** page.
     
   
   ![View Agent Details](view_agent_details_readonly.png)

6. **Configure the requested parameters:**
   
   * Confirm with the Trainers for credentials.
  
   * `IMPALA_HOST`: coordinator-churn-hol-impala-001.dw-churn-hol-cdp-env.sm02r9.b0.cloudera.site.
  
   * `IMPALA_DATABASE`: 443.
     
   * `IMPALA_USER`: Workload user assigned to you (eg. user0XX).
     
   * `IMPALA_PASSWORD`: Workload password for your user.
     
   * `IMPALA_PORT`: default.
     
     
   * Click **Save & Next**.
     
   
   ![Configure Workspace Parameters](configure_workspace_parameters.png)

*(FYI Only) Overview of the Data Base, Tables and Actual Data:*
* **CRM Database:** It has `customer_profiles` table with the below data fields: `CustomerID, Name, Gender, Age, City, Country, PlanType, TenureMonths, ARPU`.
  
* **Core Database:** It has `usage_history` table with the below data fields: `CustomerID, UsageDate, DataUsed_GB, VoiceMinutes, SMSCount, RechargeAmount`.
  
* **Product Catalog:** It has `offer_catalog` table with the below data fields: `OfferID, OfferType, OfferName, Description, Eligibility, Discount, Validity`.
  
* **Competitive Offerings:** It is a web scraper that fetches data from any given competitor website.
  

### Step 4: Test the Workflow with Sample Queries

Test the workflow with the following queries:

* *Who are our most active customers this month?*
  
* *Which customers haven’t recharged in the last 30 days?*
  


   ![Test Workflow with Sample Queries](test_workflow_queries.png)

### Step 6: Deploy the Workflow

1. Click **Save & Next** > **Deploy**.
   
2. Deployment will take approximately 5 - 7 minutes to complete.

   ![Deploy Agentic Workflow](deploy_workflow_button.png)

### Step 7: Accessing Product Workflow

1. Go to the Home Page of Agent Studios.
   
2. Select your Workflow from **Deployed Workflows**.
   
3. Click on **Open Application UI**.
   

   ![Access Deployed Application UI](access_deployed_application.png)

### Step 8: Play with your Live Application!

Test out your new Agentic AI application using sample business questions:

* *Which customers are most likely to upgrade their plan in the next 30 days?*
  
* *Which customers are eligible for loyalty rewards this month based on consistent usage and ARPU?*
  
* *What are the plans offers by [competitor telecom] \<website> ?*
  
* *How competitive are our roaming or data booster offers compared to [competitor telecom] \<website> ?*
  

   ![Live Application Chat Interface](live_application_chat_interface.png)

**End of Lab**
