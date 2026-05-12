# Security Copilot Workshop Training - Purview

*Extracted from: Security_Copilot_Workshop Training_ Purview.pdf*

---

Data Security Powered by AI (Security 
Copilot)  
Contents  
Prerequisites Guide for using Security Copilot in Purview Training  ................................ ..................  3 
Security Copilot & Purview Setup Checklist  ................................ ................................ .............................  3 
Security Copilot Prerequisites  ................................ ................................ ................................ ........................  3 
Provision Security Compute Units (SCUs)  ................................ ................................ ............................  3 
Assign Roles (If Security Copilot is enabled but you cannot use it you may need 
permission)  ................................ ................................ ................................ ................................ .......................  3 
Enable Data Sharing across M365 Data (This is required to use Purview skills)  ................  3 
Verify/Enable Purview Plugin (This is required to use Purview skills)  ................................ .. 4 
Security Copilot Agents Prerequisites  ................................ ................................ ................................ .........  5 
Understand Agent Capabilities  ................................ ................................ ................................ ..................  5 
Permissions  ................................ ................................ ................................ ................................ .......................  5 
Enabling agent  ................................ ................................ ................................ ................................ ..................  6 
Setup Agent  ................................ ................................ ................................ ................................ ........................  6 
Additional permissions for using Security Copilot skills during the workshop  ........................  7 
Lab ................................ ................................ ................................ ................................ ................................ ..................  8 
Setup agents (If not done as PreReq):  ................................ ................................ ................................ .........  8 
Enabling Agents for your tenant  ................................ ................................ ................................ ....................  8 
DLP/IRM Agent Step -by-Step Guidance  ................................ ................................ ................................ ..... 8 
Permissions  ................................ ................................ ................................ ................................ .......................  8 
Working with the agent output  ................................ ................................ ................................ ...................  12 
Microsoft Purview Data Security Posture Management (DSPM) ................................ .......................  15 
Permissions Required in Purview  ................................ ................................ ................................ .............  15 
Step -by-Step Guidance  ................................ ................................ ................................ ................................ .... 15 
Microsoft Copilot in Microsoft Purview: Data Loss Prevention  ................................ .........................  19 
Permissions required for this activity  ................................ ................................ ................................ ...... 19 
Microsoft Purview DLP Policy Insights with Copilot Step -by-Step Guidance ..........................  19 
Microsoft Purview Activity Explorer Investigation Step -by-Step Guidance  ............................  21 

Microsoft Copilot in Microsoft Purview: Insider Risk Management  ................................ ................  23 
Permissions  ................................ ................................ ................................ ................................ .........................  24 
Step -by-Step Guidance  ................................ ................................ ................................ ................................ .... 24 
Microsoft Copilot in Microsoft Purview: eDiscovery  ................................ ................................ ..............  27 
Permissions  ................................ ................................ ................................ ................................ .........................  27 
Gain Summary of an eDiscovery Case Step -by-Step Guidance  ................................ .......................  27 
Generate an eDiscovery search query Step -by-Step Guidance  ................................ ......................  29 
 
  

Prerequisites Guide for using Security Co pilot in Purview Training  
Security Copilot & Purview Setup Checklist  
1. Security Compute Units (SCUs) are available  
2. Permissions to Security Copilot are granted  
3. Security Copilot Data M365 Data Sharing is enabled  
4. Purview Plugin is enabled  
5. Permission to install Purview Agents is granted  
6. Purview Agents are enabled and set up  
7. Optional permissions in Purview for other scenarios are enabled  
Security Copilot Prerequisites  
Before the workshop , participants must complete the following steps  to follow along and 
participate : 
Make sure security copilot is enabled and you can use it in Purview. If this is already done, 
you can skip this step  and move to Agent setup.  You can verify this by trying to use Copilot 
inside of the Purview Portal. For this workshop we recommend 3 -5 SCUs for the duration of 
the workshop to be able to complete most exercises.  
Setup Security Copilot for Purview  (Get started with Microsoft Security Copilot | Microsoft 
Learn ): 
Provision Security Compute Units (SCUs)  
SCUs are required to run Security Copilot.  
Minimum: 1 SCU (recommended: 3 -5 SCUs for training).  
SCUs are billed hourly and can be managed via the Azure portal or Security Copilot portal.  
Assign Roles  (If Security Copilot is enabled but you cannot use it you may need permission)  
Ensure appropriate roles are assigned : 
• Security Copilot Contributor  or Security Copilot Owner  
You may also use the Recommended Security Cop ilot contributor roles . These roles 
determine access and ownership within Security Copilot.  
Understand authentication in Microsoft Security Copilot | Microsoft Learn  
Enable Data Sharing  across M365 Data  (This is required to use Purview skills)  
Privacy and data security in Microsoft Security Copilot | Microsoft Learn  
https://securitycopilot.microsoft.com/  > Plugin Settings > Access ing data from Microsoft 
365 Services  

 
Configure data sharing settings to allow Security Copilot to access Microsoft 365 data  which 
is required in Purview.  
Verify/ Enable Purview P lugin (This is required to use Purview skills)  
1. Go to  Microsoft Security Copilot  and sign in with your credentials.   
2. Enable the Purview plugin.   
Click on the icon on bottom right corner (boxed in red)   
  
 
• Search for Purview and enable it by toggling the control next to "Purview"   
  


 
 
Security Copilot Agents Prerequisites  
Get started with the Microsoft Purview Agents | Microsoft Learn  
Once Security Copilot is set up, participants can prepare to use Agents  setting this up ahead 
of time will allow us to be able to review agent output in the class. If these steps are not 
taken  ahead of time the agent might not complete setup in the time of the workshop : 
Understand Agent Capabilities  
Triaging and assigning priority  to alerts can be complex and time consuming. When you 
have an agent triage and prioritize alerts, according to the parameters that you set, the 
amount of time required to complete the task is reduced. The agent helps you focus on the 
most important alerts by sifting them out from the noise of lower risk alerts. This improves 
your response time and helps increase the efficiency and effectiveness of your team.  
Permissions  
There are different permissions and roles needed to perform different functions with the 
Microsoft Purview agents.   
Permissions to enable the agent (Note that the agent will run using the ID of the user who 
enabled the agent or on behalf of permissions)  
This is the minimum  permissions to enable both the IRM and DLP agent :  


• Information Protection Analyst OR Information Protection Investigator (Role 
group: Compliance Administrator OR Compliance Data Administrator OR Data 
Security Management OR Information Protection OR Information Protection 
Analysts OR Information Protection Investigators)  
• Insider Risk Management Analysis OR Insider Risk Management Investigation 
(Role group: Data Security Management OR Insider Risk Management OR 
Insider Risk Management Analysts OR Insider Risk Management Investigators)  
• Purview Content Analyst (Role group: Purview Agent Management)  
• Data Classification Content Download (Role group: Data Security Management 
OR Information Protection OR Information Protection Investigators) - needed 
for endpoint/devices DLP alerts  
• Security Copilot Contributor (Managed in Security Copilot)  
Get started with the Microsoft Purview Agents | Microsoft Learn  
Enabling agent  
This procedure is for organizations that haven't enabled any of the Microsoft Purview 
agents or have  removed agents  and you want to enable them again. Once you enable the 
agents, they're available for use in Microsoft Purview. There can be only one instance of 
each agent in a tenant. This procedure works for both the Purview DLP triage agent and the 
Insider Risk Management triage agent.  
1. Sign in to the  Microsoft Purview portal  with an account that has the  required 
permissions . 
2. In the left hand navigation pane, select  Agents . 
3. Select  Explore agents . 
4. Select the agent that you want to enable and select  Add . This opens a page that 
shows the requirements to enable the agent.  
5. Select  Setup , this opens the  Deploy agent  global configuration page. You can:  
6. Choose to  Run automatically based on a set schedule . If you don't choose this 
option, you must run the agent manually one at a time. The schedule  is set by 
Microsoft and isn't configurable by organizations. You can change this setting later 
when you edit the agent.  
7. Select the alert timeframe , which is how far back the agent looks for alerts to 
triage. Analysts can shorten the timeframe when they edit the agent but not 
lengthen it. For more information, see  Select Alert timeframe . 
8. Select  Deploy . You see the  Alert Triage Agent in <solution> is deployed  message 
when the agent is successfully deployed.  
Setup Agent  
Once an agent is enabled, you need to set specific triggers for the agent. The triggers are 
used to determine which alerts the agent triages. You can do this either in the  Agents  page 
or, for first run experience on the  Alerts  page for the solution. For this procedure, we'll use 

the first run experience  Alerts  page method. This procedure assumes that you still have the 
Microsoft Purview portal open to the  Explore agents  page from the previous procedure.  
1. Select  Go to <solution>. This opens the  Alerts  page for the solution.  
2. Because you are in the first run experience, you see dialog box that with 
a Customize  button which, when selected, opens the  Customize Alert Triage 
Agent  flyout.  
3. Here, choose either to accept the default global setting for  Select alert timeframe  or 
change it to be shorter than what was configured during agent deployment.  
4. Enter  custom instructions  for the agent. The agent interprets your natural language 
input and uses it to better identify which types of alerts matter most to you. This 
helps you identify and respond faster to the most relevant alerts.  Security Copilot 
Agents in Microsoft Purview overview (preview) | Microsoft Learn  
5. Choose  Select policies  to select the policies whose alerts will be triaged by the agent. 
In preview, all policies are selected by default, you can change that here.  
Important: The Purview DLP agent will only triage alerts from policies scoped to Exchange, 
Teams, OneDrive, and SharePoint locations. Also, the triage agents only support policies 
that use Microsoft provided  sensitive information types (SITs)  and trainable classifiers . 
6. Select  Review.  
7. Select  Start agent. Allow up to 2 hours for the agent to complete tr iaging  the in-
scope  alerts and enabled manual runs from this initial setup.  
Additional permissions for using Security Copilot skills during the 
workshop  
While these are not required,  we will do demos and walk -through  capabilities in these 
solutions that you can follow along with in your own environment.  
• DLP and MIP interactions : Information Protection Analyst OR Information 
Protection Investigator (Role group: Compliance Administrator OR Compliance Data 
Administrator OR Data Security Management OR Information Protection OR 
Information Protection Analysts OR Information Protection Investigators)  
• Insider Risk  management interactions:  Insider Risk Management Analysis OR 
Insider Risk Management Investigation (Role group: Data Security Management OR 
Insider Risk Management OR Insider Risk Management Analysts OR Insider Risk 
Management Investigators)  
• Data Security Posture Management  interactions : Data Security Viewer Role and 
IRM Admin role or Data Security Management  role group Get started with Data 
Security Posture Management | Microsoft Learn  
• eDiscovery  - eDiscovery Manager role . 

Lab  
Setup agents  (If not done as PreReq) : 
Microsoft Purview Agents offer several advanced features to enhance data security 
management. These agents provide an agent -managed alert queue that identifies and 
prioritizes the DLP and IRM alerts posing the greatest risk to an organization. They analyze 
the content and potential intent involved in an alert based on the organization’s chosen 
parameters and risk tolerance, offering a comprehensive explanation for the logic behind 
the categorization.  
The agents empower data security teams by focusing on the most important alerts and 
concentrating on critical threats. They use a dynamic process that takes input from data 
security admins and can calibrate triage results to better match the organization’s 
priorities. This ensures that critical risks are addressed first, leading to faster response 
times and improved team efficiency. These agents, powered by Security Copilot and 
Generative AI, don't take direct actions but automate the triage process for potential data 
and user risks by categorizing them as “Needs attention” or “Less urgent” and provide a 
summary of the findings. They prioritize critical alerts, continuously adapt to threats, and 
learn from feedback, enabling teams to focus on key issues and improve data security, 
compliance, and governance.  
Enabling Agents for your tenant  
Note that each agent can only be deployed once for the tenant and will be available to 
analysts that have the right permissions.  
Cost: ~.06 SCU per DLP alert and ~.04 per IRM Alert  
DLP /IRM  Agent Step -by-Step Guidance  
Permissions  
Assign the proper Roles and Permissions as follows:  
Get started with the Microsoft Purview Agents | Microsoft Learn  
Permissions for enabling the Purview DLP agent  
The account you use to enable and manage the Purview DLP agent must have all these roles:  
• Information Protection Analyst OR Information Protection Investigator (Role 
group: Compliance Administrator OR Compliance Data Administrator OR Data 
Security Management OR Information Protection OR Information Protection 
Analysts OR Information Protection Investigators)  
• Purview Content Analyst (Role group: Purview Agent Management)  
• Data Classification Content Download (Role group: Data Security Management 
OR Information Protection OR Information Protection Investigators) - needed 
for endpoint/devices DLP alerts  
• Security Copilot Contributor (Managed in Security Copilot)  

Permissions for enabling the Insider Risk Management agent  
The account you use to enable and manage the Insider Risk Management agent must have 
all these roles:  
• Insider Risk Management Analysis OR Insider Risk Management Investigation 
(Role group: Data Security Management OR Insider Risk Management OR 
Insider Risk Management Analysts OR Insider Risk Management Investigators)  
• Purview Content Analyst (Role group: Purview Agent Management)  
• Security Copilot Contributor (Managed in Security Copilot)  
 
1. Sign in to the  Microsoft Purview portal  with an account that has the  required 
permissions . 
2. In the left-hand  navigation pane, select  Agents . Select  Explore agents . 
 


3. Select the agent that you want to enable and select  Add . This opens a page that 
shows the requirements to enable the agent.  
 
4. Select  Setup  (If this is grayed out then you have not met the requirements to deploy 
the agent) , this opens the  Deploy agent  global configuration page. You can:  
5. Choose to  Run automatically based on a set schedule . If you don't choose this 
option, you must run the agent manually one at a time. The scheduled is set by 
Microsoft and isn't configurable by organizations. You can change this setting later 
when you edit the agent.  
6. Select the alert timeframe , which is how far back the agent looks for alerts to 
triage. Analysts can shorten the timeframe when they edit the agent but not 
lengthen it. For more information, see  Select Alert timeframe . 
7. Select  Deploy . You see the  Alert Triage Agent in <solution> is deployed  message 
when the agent is successfully deployed.  
 
 


8. Once the agent is deployed, You will get a success screen that you can use to quickly 
configure the agent or you can see that the alert triage agent is available for your 
organization  on the alerts page of the solution DLP or IRM.  
 
 
9. Customize the agent by clicking on Get Started . This is where you can set a lower 
lookback timeframe, enter  customer Instructions and select the policies you want 
the agent to review. Once these have been set click on Review.  
10. Leave the timeframe window or set this based on your needs  
11. Enter custom  instructions  for the Agent to consider. Example Focus on alert with 
content that contains more then 5 SSN and PII information. This is optional but can 
help the agent prioritize what you are looking for. Currently the agent only supports 
custom instructions for content and not metadata.  
12. Select any polices you want  the agent to focus on. If nothing is selected, all policies will 
be triaged.  


 
13. Review the customized triage alert agent for the alert timeframe, custom 
instructions and selected policies . If everything looks good click Start Agent . 
Otherwise click back to make any changes required.   
 
Working with the agent output  
It can take up to 2 hours for the agent to be fully deployed and start to process alerts.  
1. Once the agent has been set up, there will be a new alert queue in DLP or IRM 
depending on which agent you are in. Below is an example of DLP but this is similar 
for IRM : Solution> Alerts > Alert Triage Agent > Needs attention or Less Urgent  


 
2. In the needs attention  or less urgent  view click on an alert to get a breakdown of 
the agent’s  reasoning and insights on the alert. Review the overall Summary, 
Sensitivity risk, Exfiltration Risk and Policy risk (for DLP) or overall summary, User 
Risk, Activity Risk and File risk (IRM Alert). Notice you have the same actions you 
did in the old experience such as getting details, interacting with copilot and 
notifying users. Click on the View Details  to get even more information.  
DLP:  
 
IRM:  


 
3. In the details window you can see the details as you did before you can also get 
more information about the related assets with this alert if there are any. This could 
be files, attachments (DLP), and emails (DLP) associated with this alert. The agent 
also provides a summer of these, and analysis and provides detailed information 
about rules, match and confidence, along with any customer instructions you 
provide.  
 


 
4. Explore a couple of alerts both in the Needs attention and less urgent areas. Use the 
Thumbs up and down to provide feedback on the agent’s  reasoning and output. 
Notice how you can take all the actions you are familiar with such as Assigning and 
dismissing alerts.  
Microsoft Purview Data Security Posture Management (DSPM)   
Data security administrators can leverage Copilot for Security in DSPM to delve deeper into 
dashboard insights and conduct critical data security investigations. With Copilot, you can 
quickly uncover insights across various dimensions such as activities, files, devices, users, 
departments, or regions, enabling you to manage your data security posture more 
effectively.  
Cost ~ <0.1 -1.5 SCUs depending on what is done, time window and data.  
Permissions Required in Purview  
Data Security Posture Management:  Data Security Viewer Role and IRM Admin role or 
Data Security Management  role group Get started with Data Security Posture Management | 
Microsoft Learn  
Step -by-Step Guidance  
1. Go to the purview portal - https://purview.microsoft.com/  and sign in with your 
credentials.   


 
2. Navigate to solutions -> Data Security Posture Management  
3. We have provided promptbooks and a Prompt gallery to get you started with end -
to-end investigation along with giving you over 200 prompts that you can use to 
help with investigations.  
 
4. Click Get Started under the risky user investigation Promptbook to explore the 
prompts and inputs.  


 
5. You can run an investigation on a user for 30 days to see the experience  if you like . 
Review the output in the right copilot window. Cost ~1 SCU  
 
6. On the main screen click on View more in the prompt gallery.  


 
7. Explore the Prompt gallery to get an idea of what type of questions prompts you can 
run in DSPM. Explore the filters to get an idea of the different areas you can 
investigate. Click on a few of these prompts to run them. Cost ~0.1 SCU  per prompt  
 
Use the feedback within Copilot to tell us if the responses are accurate or not.  
For more information on writing Security Copilot prompts, go to  Microsoft Security Copilot 
prompting tips  . For enhanced experience with Copilot in DSPM, we recommend adhering to 
the following guidelines - 
• Questions involving a certain user should always include the user's UPN.  


• Questions involving a certain type of sensitive info type or label should specify the 
complete name for the sensitive info type or label for higher accuracy in response.  
• Questions where you want to get some top users/activities/alerts etc. should clearly 
list the sorting criteria for higher accuracy in response.  
• Questions where you're looking for data in a certain timeframe, please specify that 
timeframe because by default we will look back to only 10 days. The max. lookback 
we can support is 30 days  
• Entities (OOB/Custom SITs/TC/Label) to be put in single quotes in prompt  
• Any path (eg. file path) mentioned in the user prompt must use "/" as separator, 
NOT " \". 
• The accuracy of response will be higher if it's asking a single intent. If user has a 
complex question, it is advised that user should break it into single intent questions, 
and ask it one by one (sequentially)  
• User questions should be self -contained. For higher accuracy, avoid giving reference 
to previous questions or response.  
• Avoid using generic terms, user questions with product specific terms will have 
higher accuracy.  
• You can ask questions about data security across information protection, data loss 
prevention and insider risk management or get a summary from public 
documentation.  
Microsoft Copilot in Microsoft Purview: Data Loss Prevention  
After investigating using the standalone experience, let's explore the embedded experiences 
touching Data Loss Prevention. As a compliance administrator, the embedded environment 
makes it easier to get detailed data on generated alerts, policies, and activities. These 
integrations reduce the time spent understanding alerts by providing summaries, which is 
particularly helpful when learning a new product set. Even if you're familiar with alerts, 
activity explorer, and handling DLP policies, these features help bridge the knowledge gap. 
Let's see how to use these capabilities.  
Permissions required for this activity  
Information Protection Analyst OR Information Protection Investigator (Role group: 
Compliance Administrator OR Compliance Data Administrator OR Data Security 
Management OR Information Protection OR Information Protection Analysts OR 
Information Protection Investigators)  
Microsoft Purview DLP Policy Insights with Copilot Step -by-Step Guidance   
Cost ~.5 SCUs depending on number of policies  
We know that there might be several DLP policies in an organization and that it can be 
challenging to understand the coverage of these policies. With DLP policy insights, using 
Security Copilot, administrators can invoke the policy insights skill to understand and 

comprehend the insights from all their policies or even a handful of selected polices. The 
insights offered start with a higher -level view of how their policies:  
• are effective across locations  
• detect the presence of what sensitive information types throughout their digital 
estate  
• how administrators are notified of violations  
• how users are educated while they perform activities they should not  
These insights are offered with different pivots by location, classification, and by 
administrative scopes. This is offered to give the security policy administrators different 
views for deeper understanding of policy constructions  and their impact.  
1. Navigate to the DLP Policies – Data loss prevention solution > Policies  
2. Select the policies on which you would like to get insights . Click on the Copilot drop 
down and select get insights on existing policies .  
 
3. You will see the prompt is already pushed into the copilot experience in the side 
panel.  Copilot responds with insights on the selected policies  


 
4. You can ask additional prompts here such as:  
• Can you provide more details on the specific PII and financial information the 
policies are protecting?  
• What are the custom classifiers that are used in these policies?  
• Who initiated the policy updates in the last 30 days?  
• Please provide a summary of all the Data Loss Prevention (DLP) policies in our 
tenant?  
• I want to comply with GDPR across all workloads. Does this policy cover that?  
• I want to protect credential leakage over email. Can this policy do that?  
• Which users or groups are targeted by the policy?   
• What actions are taken when this DLP policy is violated?  
Microsoft Purview Activity Explorer Investigation Step -by-Step Guidance  
Cost ~.5 SCUs depending on data re turned and number of prompts   
Compliance administrators can use activity explorer to understand what is happening in 
their environment. With security copilot built -in, they can now use this help with queries 
and getting summary information quickly from the data.  
1. Go to the new Purview portal at ( https://purview.microsoft.com ) and sign in with 
your credentials.    
2. Go to the Data Loss Prevention solution and navigate to Explorers and then, Activity 
explorer.   


 
3. Along the top, you have Copilot buttons. Click on ‘Show me the top 5 activities in the 
last week”  
 
4. Play with some of the other recommended prompts.  
5. You can also use this to help write queries back on the page. Paste: “According to 
Purview, Filter and investigate "Label changed"”. Click Apply  


  
6. Notice how this filters the view on the left 
 
Microsoft Copilot in Microsoft Purview: Insider Risk Management  
Like the DLP embedded experience, a compliance admin can use Insider Risk Management 
alerts to swiftly grasp potential issues by noting crucial user details like resignations, 
exfiltration activities, patterns, roles, and anomalies. This AI -driven summary aids security 
teams in focusing on critical evidence and investigation pathways. Follow these instructions 


to learn to use this summary feature, which helps newcomers to this technology quickly 
understand the product.  
Cost ~0.5 SCUs depending on the amount of data in the alert  
Permissions  
Insider Risk Management Analysis OR Insider Risk Management Investigation (Role group: 
Data Security Management OR Insider Risk Management OR Insider Risk Management 
Analysts OR Insider Risk Management Investigators)  
Step -by-Step Guidance  
1. Go to the new Purview portal at https://purview.microsoft.com ) and sign in with 
your credentials.   
2. Go to the Insider Risk Management solution  and click on Alerts  
  


3. Choose the alert you want to review. And click on the Copilot Icon to get a summary  
 
 
4. From the Copilot prompt, click on the book icon and review the list of available 
prompts, select any prompt to dive deeper into user activity (you can select any 
recommended prompts from the list). In the example below, we’ll run "Did the user 
engage in any unusual behavior? ” and “Summarize user’s last 30 days of activity”  and 
review the results.  


   
5. You can also look at users in IRM and get a summary of their risk based on all their 
alerts. If you go to the Users tab. Select a user and click on Summarize with Copilot .  
 


 
Microsoft Copilot in Microsoft Purview: eDiscovery  
eDiscovery is a tool that helps organizations identify, review, and manage electronically 
stored information for legal cases and investigations. It allows users to search for content 
across various Microsoft 365 services, place holds on relevant data, and export search 
results for further analysis. With the integration of Security Copilot, the goal is to simply and 
reduce the amount of time needed to get information from eDiscovery.  
Cost ~  0.75 SCUS depending on complexity and number of prompts  
Permissions  
eDiscovery  - eDiscovery Manager role.  
Gain Summary of an eDiscovery Case Step -by-Step Guidance  
 
1. Navigate to the Purview portal (purview.microsoft.com) open the eDiscovery 
Solutions and go to the Cases subsection under eDiscovery.   


 
2. Open any case. In this example, we’re opening the case titled “ MVP Summit 2025” 
(Or create a new case) Click on Summarize this case . 
3. This will give you and overview of the case, case details like the settings, Jobs, 
Searches, Data sources, review sets, holds and exports.  
 
4. Look at the follow -up prompts to dive into the summary more.  


 
Generate an eDiscovery search query Step -by-Step Guidance  
1. In this case either create a new search or use a search that already exists.  
2. To create click Create a search. Give it a name and select Create.  Note: Any case can 
be used, the goal is to create a search.  


  
3. Click “Draft a query with Copilot”   
   
4. Provide your own natural language input or select one of the suggested prompts. 
Example : “Find all the emails that have the words confidential and budget with 
attachments in the last year”   


  
5. Click “Refine” to optimize your natural language input for Security Copilot. Either 
accept or discard the suggested refinement.   
  
6. Click “Generate KQL” to generate a search query from the natural language input.   


  
 


