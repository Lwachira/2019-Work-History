# 2019 Work History

 > **Sadly due to complicate legal requirement's I am not allowed to share the source code from [2016](https://github.com/Lwachira/2016-Internship), [2018](https://github.com/Lwachira/2018-Work-History), [2020](https://github.com/Lwachira/2020-Work-History) with you. If you wish to pursue this further, we should chat, I can explain all the interesting things I built over the last 3 years**.
## What is this?

The work here is a representation of the work I did in 2019. After proving myself in [2018](https://github.com/Lwachira/2018-Work-History) with the work I did. I had the opportunity to work on other problems the business had. 

I have four projects that used by the company internally and three Projects that did not see the light of day to complicated business reason and no failure on my part.


### Table of Contents
- [Dynamics Logger](#dynamics-logger)
- [LeadLogger](#leadlogger)
- [SiebelCRM365](#siebelcrm365)
- [SiebelExtraction](#siebelextraction)
- [Failed Projects](#failed-projects)
    - [SiebelContractLogger](#siebelcontractlogger)
    - [SiebelExchangeLogger](#siebelexchangelogger)
    - [PODTracker](#podtracker)
    

# Dynamics Logger

One of the business problems I had solve was an issue of lack of automation with user tickets. Tickets would come in the form of Emails and need to be added to the companies **Microsoft Dynamics 365 CRM**. 

This software solves that in the following way: 
1. Software scans email address using the Microsoft Exchange Web Service
2. Once it finds all the emails it needs to process it loads them to memory. 
3. It takes each email, logs it to CRM then moves the email to a done folder on the email account if both are successful.
4. It updates a database table with the metadata of the email.
5. Managers can use the database tables to build reports improve business processes.


# LeadLogger

Another problem the marketing team had was with capturing leads done on different company sites. I created two programs: 
- The first being a Web API program that listens for postback responses from an html form and pushes the formdata into a database table.

- The second being a Windows Console application that works in the background, it reads the data in the tables and copies them to the Siebel CRM for the marketing team to use.

# SiebelCRM365

This one is my favorite. The business had this legacy piece of software. Before I started working on it, its uptime was roughly 20% with numerous bugs (work was duplicating and not functioning as intended)

Similar to the [Dynamics Logger](#dynamics-logger) this worked by reading emails, updating Siebel/Oracle CRM Service Requests and moving the emails to a done email folder. 

> I solved the duplication problem by creating a log table that uses SQL to identify if the email was previously processed then we ignore it else we process the email.

# SiebelExtraction

# Failed Projects

## SiebelContractLogger

The application built and the team (myself and manager) ready to launch, then one of the execs got scared, made a whole thing about the risk and said they will get back to us, until to this day we are still waiting...

## SiebelExchangeLogger

This was the original SiebelCRM Logger that was replaced by my SiebelCRM365, the original made use of on prem Exchange servers, which were scheduled for decommission end 2019, fortunately we knew this was happening and planned accordingly (sorry no crazy coffee story)

## PODTracker

This one was fun; the business had this mundane task of checking proof of delivery (POD) number site by site. What we needed to build was something that pings each site using the POD number, if it got a hit then win else lose. Sadly, some sites were pure single page applications (SPA) so we had can this project. I ended up using selenium to build this.
