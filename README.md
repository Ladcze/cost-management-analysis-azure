# Introduction 
Here a quick guide on how to use cost analysis to better understand how your costs accrue each month. With this understanding, budgets can be created within an Azure tenant/resources to help monitor and alert on your costs associated within scoped resources.

--- 

# Objectives
- Understand Cost Management best practices. You want to analyze which resources are the primary drivers of your monthly bill. Another key goal is to set thresholds on your team's Azure expenses to help stay within a budget.
- Analyze costs on a subscription using cost analysis
- Create your first Azure budget based on your analysis

--- 

# Prerequisites/Services deployed
- An Azure subscription
- A number of Azure resources created within your subscription that have been accruing cost for at least one month
- Cost management tool/service

--- 

# Basic Principles of Cost management
- What is an Cost Management?   
Microsoft Cost Management provide tools to plan for, analyze, and reduce your spending to maximize your cloud investment. 
It is easy to build and deploy cloud solutions across Azure. However, it's important that those solutions are optimized to minimize the cost to your organization. 
 
- Evaluating costs using cost analysis 
There are also many ways you can customize cost views for deeper analysis. These include: 
  - Accumulated cost view
  - Actual cost
  - Forecast
  - Budget
  - Pivot (donut) charts

- Cost analysis also provides options to save and share cost-analysis views. Also, data from cost analysis can be exported for use elsewhere.

 ---
 
# Determine your most expensive resource and see trends
Steps (in summary)
- Sign in to the Azure portal 
- Navigate to Cost analysis.
- Group results by resources.
- Adjust date range and granularity
 
Sign in to the Azure portal   
![image](https://github.com/Ladcze/cost-management-analysis-azure/assets/97769275/44852247-1cd9-4bd1-8032-aa9a73dcf471)
 
Navigate to Cost analysis.
In the portal search box, enter Subscriptions.
In the list of services, select Subscriptions.
In the list of subscriptions, select a subscription.
In the menu pane under Cost Management, select Cost analysis.
![image](https://github.com/Ladcze/cost-management-analysis-azure/assets/97769275/79d2460e-0c1c-4609-9fe6-fcb9e464f065)
 
Group your results to view resources.
Select the Group by list to view a list of values to filter by, then select Resource.   
![image](https://github.com/Ladcze/cost-management-analysis-azure/assets/97769275/db905d93-a45b-4cb9-928c-f70217e11d39)   

![image](https://github.com/Ladcze/cost-management-analysis-azure/assets/97769275/ec97cc6e-0ff6-4718-9a1a-5c293345636d)   


Adjust results to find your most expensive resources.
Select the Granularity item to view a list of time grain values to filter by (Daily).
![image](https://github.com/Ladcze/cost-management-analysis-azure/assets/97769275/5a6712a3-173b-4451-8f82-19faf0dc36f8)   
Select the date list item (calendar symbol) to view available date ranges, and then under Calendar months, select Last 3 months.   
![image](https://github.com/Ladcze/cost-management-analysis-azure/assets/97769275/ee96d893-7eca-4b35-86e8-a80ccc18be0a)

In this instance Storage1 appears to be the resource with highest cost. The  resource name (resourceID) should be noted as this will be required later in readiness for creatign our budgets.   
You can also Look for trends in specific resource costs over time.

---

# Creating a budget
Steps (in summary)
  - Sign in to the Azure portal 
  - Navigate to Budgets
  - Configure your budget
  - Configure a budget alert threshold

Sign in to the Azure portal   
![image](https://github.com/Ladcze/cost-management-analysis-azure/assets/97769275/b9d2c25f-f37e-48ed-8db7-fe7af554f885)

Navigate to Budgets
In the portal search box, enter Subscriptions.
In the list of services, select Subscriptions.
In the list of subscriptions, select the subscription that you analyzed in the previous exercise. The subscription contains your most expensive resource.
In the menu, under Cost Management, select Budgets. The Budgets pane appears.
![image](https://github.com/Ladcze/cost-management-analysis-azure/assets/97769275/d661ec71-4aa0-4106-ad2e-01b0448805fc)


Configure your budget
From the top menu, select Add, and then, under Budget scoping, select Add filter.
From the Filter dropdown list, select ResourceId.
In the selection dropdown list, select your most expensive resource that you identified in the previous exercise. A suggested budget appears. The budget is associated with your selection.
Name your budget (for example: Storage1-Budget).
Set the Reset period to Monthly.
Examine the Budget Amount recommendation based on your filter. Then, analyze the View of monthly cost data graph to determine if the threshold meets your needs.
Optionally, change the budget amount to any value that you like.
When you've decided on a budget amount, select Next.


![image](https://github.com/Ladcze/cost-management-analysis-azure/assets/97769275/94dc2b25-c7c9-476c-856e-083d71f35f48)

Configure a budget alert threshold
Lastly, configure a budget threshold, and specify an email address for alert notification.
Configure the alert condition for 90% of the budget. Don't specify an action group.
Enter your email address in the Alert recipients (email) section.
Examine the View of monthly cost data graph, and verify that the alert threshold is correct.
Select Create.

![image](https://github.com/Ladcze/cost-management-analysis-azure/assets/97769275/f44b7990-4927-4702-ad27-75434d381fd5)

![image](https://github.com/Ladcze/cost-management-analysis-azure/assets/97769275/6abe23a9-61b0-4b2f-a857-2348453cb070)


---

# Summary
This has been a quick run through the Cost Management principles and basic concepts which should help manage costs within Azure.
We've evaluated costs of some Azure resources using cost analysis and looked at costs in detail. 
The data generated can be exported and used outside of Azure. With cost analysis tools, we can track/identify the most expensive Azure resource and investigate cost trends. 
On a final note, budget(s) have been set against scoped resources to help keep costs under control; and alerts have also been setup notify specified recipients.  

---

# References:   
https://learn.microsoft.com/en-us/training/modules/analyze-costs-create-budgets-azure-cost-management/

