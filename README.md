
# DO NOT SHARE NOTICE:

> This is a **living developer guide** that will undergo multitudinous modifications/adjustments as development progresses. All commits/pushes/modifications are recognized by the contributing author and attributed as applicable. Since this software **IS PROPRIETARY**, this document will **NOT BE SHARED** unless authorization is warranted from Brantley Pace (CEO) and/or JJ McMillen (Creative). **NO EXCEPTIONS** are authorized.
 > 
# Approved Editors:
* Brantely pace, CEO
* JJ McMillen, Creative 
* Charles Arcodia, CTO
* Sam Blount, AE


# Overview: Project getupsell.com 
* Empower your revenue generating teams to become product experts with intuitive analytics insights, intelligently organized into tasks. Know your customers' needs before they do.
* Traditionally, Account Executives have very little visibility on how customers are using their products. Because of that, companies sell less than they could and customers are left with “just checking in emails.” Our mission is to help companies grow existing business by empowering their sales teams with product usage insights.

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

 
 # Primary Development Machine
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
 > GDPR is responsible for data security and protecting the end users. Since the penalties for non-conformity is high, please read through the guidelines @ https://gdpr-info.eu for further understanding. The General Data Protection Regulation (GDPR) is the toughest privacy and security law in the world. Though it was drafted and passed by the European Union (EU), it imposes obligations onto organizations anywhere, so long as they target or collect data related to people in the EU. The regulation was put into effect on May 25, 2018. The GDPR will levy harsh fines against those who violate its privacy and security standards, with penalties reaching into the tens of millions of euros.

 > With the GDPR, Europe is signaling its firm stance on data privacy and security at a time when more people are entrusting their personal data with cloud services and breaches are a daily occurrence. The regulation itself is large, far-reaching, and fairly light on specifics, making GDPR compliance a daunting prospect, particularly for small and medium-sized enterprises (SMEs).








# Deebly Integration START (2 Signals)

 **URL for Testing**
 
    https://salty-savannah-91118.herokuapp.com

# Endpoint

    /deebly_signals
 
# Complete URL

    https://salty-savannah-91118.herokuapp.com/deebly_signals

# Headers

    application/json  Content-Type
    application/json  Accept
 
 # HTTP Method
 
    POST
    
 #  Deebly integration requires 3 keys to be integrated into the Deebly platform. 
 
 > First key (new_client_registration): Triggered when a new client registers for the Deebly platform. 
 > Second key (new_client_paid_plan): Triggered when a new client engages a paid plan.
 > Third key (client_total_spend_increase): Triggered when a new client moves money to the Deebly platform.
 > Every parameter is of type 'string' except for is_development_key is of type bool.

1. new_client_registration (Place API call into the function that registers new users into the Deebly platform)

      **required parameters
         
         "admin_key" :  "Grab this from the dashboard - endpoint /developer_keys under Keys/Development",
         "is_development_key": Set this to true, as BETA will take place under development,
         "type_of_key" : "new_client_registration",
         "bdr_user_uid" : "This is the Business Development Reps unique UID stored in the Deebly Database - for example, Barry's UID", 
         "bdr_client_uid" : "This is the Business Development Reps client unique UID stored in the Deebly Database", 
         "bdr_client_email" : "This is the Business Development Reps client's email
 
    
 2. new_client_paid_plan (Place API call into the function that registers the client for a paid service)

      **required parameters
         
         "admin_key" :  "Grab this from the dashboard - endpoint /developer_keys under Keys/Development",
         "is_development_key": true,
         "type_of_key" : "new_client_paid_plan",
         "bdr_user_uid" : "This is the Business Development Reps unique UID stored in the Deebly Database - for example, Barry's UID", 
         "bdr_client_uid" : "This is the Business Development Reps client unique UID stored in the Deebly Database", 
         "bdr_client_email" : "This is the Business Development Reps client's email,
         "type_of_paid_plan" : "The name of the registered plan the user signed up for"
    
 3. client_total_spend_increase (Place API call into the function that moves money on behalf of the client)

      **required parameters
         
         "admin_key" :  "Grab this from the dashboard - endpoint /developer_keys under Keys/Development",
         "is_development_key": true,
         "type_of_key" : "client_total_spend_increase",
         "bdr_user_uid" : "This is the Business Development Reps unique UID stored in the Deebly Database - for example, Barry's UID", 
         "bdr_client_uid" : "This is the Business Development Reps client unique UID stored in the Deebly Database", 
         "bdr_client_email" : "This is the Business Development Reps client's email,
         "type_of_paid_plan" : "The name of the registered plan the user signed up for",
         "client_total_spend" : "Place the monetary value that the client pays everytime a payment is made"
 
 
 # Deebly Integration END (2 Signals)
 
 # Integration
 
    With Upsells API, users can manage tasks using simple HTTPS rest calls with preset parameters depening on the needs of the organization for global API access. 

    For clarity, our REST API is designed and patterned using HTTP protocol.

    For HTTP basic authentication and communication with the upsell servers, users will provide bare minimum credentials such as their Company Email along with        their Phone number. From here, an account is created with the appropriate development/production keys to access our systems.  

    From here, developers will implement HTTP calls to dev.getupsell.com along with the appropriate parameters. As an example, the average logo requires 5 keys (5 API Calls) with an integration time of under 1 hour. 

    After integration, the Admin can assign user credentials, rotate API keys and conduct task management. The BDR’s will follow their Upsell tasks accordingly and archive when necessary. 

    Please refer to an example implementation of an HTTP call using Swift. 

 
 # iOS Swift Singleton Example 
 
    import Foundation

    class Service : NSObject {
   
    static let shared = Service()
    
    func upsellPostRequest(admin_key: String, is_development_key: Bool, type_of_key : String, completion: @escaping ([String: Any]?, Error?) -> Void) {
        
        let parameters : [String : Any] = ["admin_key": admin_key, "is_development_key": is_development_key, "type_of_key" : type_of_key]
        
        let slug = "targeted_request_key"
        
        let url = URL(string: "https://salty-savannah-91118.herokuapp.com/\(slug)")!
        
        let session = URLSession.shared
        
        var request = URLRequest(url: url)
        request.httpMethod = "POST"
        
        do {
            request.httpBody = try JSONSerialization.data(withJSONObject: parameters, options: .prettyPrinted) // pass dictionary to data object and set it as request body
        } catch let error {
            print(error.localizedDescription)
            completion(nil, error)
        }
        
        request.addValue("application/json", forHTTPHeaderField: "Content-Type")
        request.addValue("application/json", forHTTPHeaderField: "Accept")
        
        let task = session.dataTask(with: request, completionHandler: { data, response, error in
            
            guard error == nil else {
                completion(nil, error)
                return
            }
            
            guard let data = data else {
                completion(nil, NSError(domain: "dataNilError", code: -100001, userInfo: nil))
                return
            }
            
            do {
                
                guard let json = try JSONSerialization.jsonObject(with: data, options: .mutableContainers) as? [String: Any] else {
                    completion(nil, NSError(domain: "invalidJSONTypeError", code: -100009, userInfo: nil))
                    return
                }
                completion(json, nil)
            } catch let error {
                print(error.localizedDescription)
                completion(nil, error)
            }
        })
        
        task.resume()
      }
    }




 # Developer and Integration Guide (HTTPS and REST API for Logo Integration)
 
 **URLS for Testing and Production**
 * Development URL : https://dev.getupsell.com/
 * Production URL : https://prod.getupsell.com/
 
 
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

# How to get the Development and Production Keys
 1. Make a company account @ app.getupsell.com
    * Company Name
    * Company Email
    * Password

2. Hover over Developer Portal
    * Select Developer Keys
    * Make a secure copy of the Developer/Production Keys (60 character string)
 

 # Developer Portal
 * Dev and Prod Keys
 * Access to development logs and permissions
 * Correlated Tasks for the correct user

 **STACK**
 Plain and Vanilla HTML
 Javascript
 Database Connectivity - MongoDB and Firebase

 # Developer Guide Creator and Licensing: Monday May 10th, 2021

 **Project Manager/Salesforce Developer**
 * Project Manager: Brantley Pace
 * LinkedIn: https://www.linkedin.com/in/brantley-pace/
 * Email: brantley@getupsell.com
 * Education: MBA

 **CREATIVE**
 * Design/UI/UX: JJ McMillen
 * Email: jennifer@getupsell.com
 * LinkedIn: https://www.linkedin.com/in/jennifer-mcmillen/
 * Education: Masters of Art, Design for Sustainability
  
 **Chief Technology Officer**
 * CTO/Developer: Charles Arcodia
 * Email: charliearcodia@gmail.com
 * LinkedIn: https://www.linkedin.com/in/charlie-arcodia-5b7898114/
 * Education: MBA/CS
 * Languages: C#, C++, JavaScript, Swift, Kotlin

 **Account Executive**
 * AE: Sam Blount
 * Email: sam@getupsell.com
 * LinkedIn: https://www.linkedin.com/in/samblount/

# Licensing for Source Control
* License: APACHE LICENSE, VERSION 2.0 (2004) - https://www.apache.org/licenses/LICENSE-2.0.html
