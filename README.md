
# DO NOT SHARE NOTICE:

> This is a **living developer guide** that will undergo multitudinous modifications/adjustments as development progresses. All commits/pushes/modifications are recognized by the contributing author and attributed as applicable. Since this software **IS PROPRIETARY**, this document will **NOT BE SHARED** unless authorization is warranted from Brantley Pace (CEO) and/or JJ McMillen (Creative). **NO EXCEPTIONS** are authorized.
 > 
# Approved Editors:
* Brantely pace, CEO
* JJ McMillen, Creative 
* Charles Arcodia, CTO


# Overview: Project getupsell.com 
* Empower your revenue generating teams to become product experts with intuitive analytics insights, intelligently organized into tasks. Know your customers' needs before they do.
* Traditionally, account executives have very little visibility on how customers are using their products. Because of that, companies sell less than they could and customers are left with “just checking in emails.” Our mission is to help companies grow existing business by empowering their sales teams with product usage insights.

 # Living Overview and key Fundamentals (Google Doc Overview)
 https://docs.google.com/document/d/1oZd0UF7xCtHNjL666cglS_HRMJAUVVgwSerWU5AkCls/edit

 # Source/Version Control
 * GitHub (Preferred)

 # Website

 * https://www.getupsell.com

 # Accompanying links for development and references

 * https://console.firebase.google.com/u/0/

 * https://nodejs.org/en/
  
 * https://code.visualstudio.com
  
 * https://atom.io
  
 * https://gdpr-info.eu

 * https://firebase.google.com/docs/storage

 
 # CTO Primary Development Machine
 * iMac Pro - Big Sur V 11.1
 * Processor 3.2 GHz 8-Core Intel Xenon W
 * Memory 32 GB 2666 MHz DDR4
 * Graphics Radeon Pro Vega 56 8 GB

 # Backend IDE/Syntax
 * Visual Studio Code/Atom IDE's
 * Node.JS - https://nodejs.org/en/
 * JavaScript
 * Firebase Database
 * Firebase Storage
 * Firebase HTTPS Cloud Functions
 * Heroku - https://dashboard.heroku.com/apps
 * Mongo Database - https://www.mongodb.com

 # 3rd Party Frameworks (Subject to change as necessary)
  
 * Express
 * Morgan
 * Firebase Storage
 * Firebase Database
 * Mongo DB (Database)

 # GDPR (General Data Protection Regulation) and pertatining rules for development
 > GDPR is responsible for data security and protecting the end users, in this case the clients who will be getting their dogs groomed. Since the penalties for non-conformity is high, please read through the guidelines @ https://gdpr-info.eu for further understanding. The General Data Protection Regulation (GDPR) is the toughest privacy and security law in the world. Though it was drafted and passed by the European Union (EU), it imposes obligations onto organizations anywhere, so long as they target or collect data related to people in the EU. The regulation was put into effect on May 25, 2018. The GDPR will levy harsh fines against those who violate its privacy and security standards, with penalties reaching into the tens of millions of euros.

 > With the GDPR, Europe is signaling its firm stance on data privacy and security at a time when more people are entrusting their personal data with cloud services and breaches are a daily occurrence. The regulation itself is large, far-reaching, and fairly light on specifics, making GDPR compliance a daunting prospect, particularly for small and medium-sized enterprises (SMEs).


 # Developer and Integration Guide (HTTPS and REST API for Logo Integration)
 
 **URLS for Testing and Production**
 * Development URL : https://salty-savannah-91118.herokuapp.com/
 * Production URL : https://salty-savannah-2-91118.herokuapp.com/
 
 **Endpoints:**
 * /company_authentication
 * /manage_users
 
 **company_authentication**
 *The first time a company/logo integrates getupsell with their current platform, company_authentication needs to be called with the following parameters:*
 
 *String*
  * type_of_request 
  * email
  * password
  * displayName
  * sign_up_date
  * user_uid

        - type_of_request can either be: "registration" || "registration_database_update"

 **registration**
  * type_of_request 
  * email
  * password
  * displayName

**registration_database_update**
  * type_of_request
  * email
  * sign_up_date
  * user_uid

 **manage_users**
  * companyUID
  * user_UID
  * user_first_name
  * user_last_name

 # Developer Guide Creator and Licensing: Monday May 12th, 2021

 **Project Managers/Salesforce Developer**
 * Project Manager: Brantley Pace
 * LinkedIn: https://www.linkedin.com/in/brantley-pace/
 * Email: brantley@getupsell.com
 * Education: MBA

 **CREATIVE**
 * Design/UI/UX/: JJ McMillen
 * Email: jennifer@getupsell.com
 * LinkedIn: https://www.linkedin.com/in/jennifer-mcmillen/
 * Education: Masters of Art, Design for Sustainability
  
 **CTO**
 * CTO/Developer: Charles Arcodia
 * Email: charliearcodia@gmail.com
 * LinkedIn: https://www.linkedin.com/in/charlie-arcodia-5b7898114/
 * Education: MBA/CS
 * Languages: C#, C++, JavaScript, Swift, Kotlin

# Licensing for Source Control
* License: APACHE LICENSE, VERSION 2.0 (2004) - https://www.apache.org/licenses/LICENSE-2.0.html
