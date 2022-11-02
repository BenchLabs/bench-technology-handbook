# Bench Test Accounts

[Introduction](#introduction)   
[Square](#Square)  
[Shopify](#Shopify)  
[Stripe](#Stripe)  
[Gusto](#Gusto)  
[Plaid](#Plaid)  
[FileThis](#FileThis)  

## Introduction:
App Support has access to tools and data that positions us well to create high quality testing accounts. 
This document will serve as a guide for which connections can be set up for test accounts. 

BAS have created **two** readily available testing accounts in Staging and Production that **anyone across TPD can use**. 

You can find the details of these accounts [here](https://docs.google.com/spreadsheets/d/1ACn2K5nxmgYNUeIIjmGsW0IPoOLuXpFKgTWFMdey_cI/edit?usp=sharing), and a guide on how to create similar high quality testing accounts at the bottom of this document.

#### Test connections availability chart 
*[x] = methods of adding test connections are available*
| Integration  | Staging | Production |
| ------------- | ------------- | ------------- |
| Square  | [x] | [ ] |
| Shopify  | [ ] | [x] |
| Stripe  | [x]  | [x] |
| Gusto  | [x] | [ ] |
| Plaid  | [x] | [ ] |
| FileThis  | [ ] | [ ] |

### Connection Setup Instructions:

## Square	

#### Staging
1. Sign into a Bench staging account
2. Visit [this link](https://developer.squareup.com/apps) and log in using the Square API Development credentials
3. Scroll down to the  Sandbox Test account section and click on Open by Default Test Account
4. In the Bench App Go to Account> Connections > Click 'Add+' by Square
5. The Bench App should be open in a new tab in the same window for this to work
6. Click allow if a screen similar to the one below shows up
![alt text](https://i.imgur.com/WOYUnY3.png "Square Connection Page")

#### Production
N/A. We do not have access to a clients account we can use for testing this in production anymore. 

## Shopify
 
#### Staging
It is not possible to connect this through Staging. 
After you connect the app in Shopify, it redirects you to bench.co to finalize the connection, and staging's URL is 10sheet.ca, not bench.co.

#### Production
Shopify costs $26/ month to have an open account, but you can set up a free trial account to test adding connections. Shopify test credentials can be found in the Engineering 1Pass vault for `luke.gartland@bench.co`, but the account there has an elapsed free trial. So we’ll need to set up a new store.

1. Create a Shopify account, or log in using the luke.gartland@bench.co one, and click on the User profile and then Stores. 
2. Click ‘Create another Store’. Proceed through the sign up flow to set up the store correctly. 
3. You can now go back to the Bench App, sign in as a client, go to Account > Connections and click the ‘Add +’ next to the Shopify section. 
4. Enter in your credentials for Shopify and select your new store and click on “Add app” to finalize the connection. 

## Stripe
Adding a card
#### Staging
1. Log in as a client and go to your Billing page in Settings. 
2. Click ADD CARD, input the testing credentials found on Stripe’s Testing Documents [here](https://stripe.com/docs/testing#cards) and click SAVE.

#### Production
N/A. There is no way to test adding a card to the Bench app via Stripe in production without adding a real card.

Adding a connection 
#### Staging/ Production
You can add a Stripe account to Staging or Production by creating a fake Stripe account. 
If you are creating your own fake Stripe account, you will be presented with a page that asks for a valid routing number and institution number. 
I was able to trick it by using some generic test routing numbers I found online and some random string of numbers for the institution number. 
I have left the credentials for one in the Engineering 1Pass under ‘luke.gartland+StripeBASTest@bench.co’. 

## Gusto
#### Staging

Gusto have previously told us they do not provide test accounts, however they do have a [live demo account](https://app.gusto-demo.com/payroll_admin) for people curious about their product. I was able to connect the Gusto demo account to the Staging client by taking the following steps:

1. Open up the test client in Client View and go to Account Connections. 
2. Click Add + next to Gusto. 
In another tab go to Gusto’s [documentation page](https://docs.gusto.com/app-integrations/docs) and click ‘Gusto Sandbox’ in the sidebar. This will open the following link: https://app.gusto-demo.com/login
3. The page will redirect then to the authorization page and you can authorize the connection with the sandbox account.

_I have been able to link this demo account to multiple test accounts._

## Plaid
#### Staging
1. Sign in to a staging Bench account as a client. 
2. Navigate to Account > Connections and click the ‘Add +’ next to the ‘Link Banks and Credit Cards’ prompt. 
3. The Plaid modal will pop up. Select any institution, it does not matter. 
4. Enter in the credentials found [here](https://plaid.com/docs/sandbox/test-credentials/) for the username and password. 
5. Select the account(s) you wish to track. These are all fake accounts and the values never change. 

#### Production
We do not have Plaid testing credentials for production. Plaid’s production environment requires real bank accounts. 

### Documentation
Plaid's guide to testing multiple connection flows + creating customized user data can be found [here](https://plaid.com/docs/sandbox/test-credentials/)

## FileThis
We do not currently have a way of adding test credentials for FileThis/ Statement Importer yet but we believe there is a way if we just add the heroku test app that FileThis uses for testing to our api list of filethis institutions. More slack context can be found [here](https://bench.slack.com/archives/C4RKU26H3/p1666893357681159)

## Steps for creating a high quality testing account	

1. Create a new account in the client management tool in the environment you want to test in. [Production link](https://dashboard.in.bench.co/client-management/), [Staging link](https://dashboard.in.10sheet.ca/client-management/). 
2. Assign any primary user for now and note the client id. 
3. Open the client in BKTools and in Client View. Use the steps above to create test connections.
4. Go to client details in your test client. Scroll to the bottom to disable ‘Zero-state reports’ (this will soon be handled through Split). 
Optional: If you need to use FLO for this client, assign yourself as any role under the ‘Team’ section and open Flo through Okta. 
3. Go to Ledger Accounts. Click ‘New Ledger’, then toggle ‘Functional Ledger’, then fill out the details of a Checking account (Category: **Assets**), a Credit account (**Liability**), Gusto (**Operating Expense**), Stripe (**Add-on**) as desired. 
4. Go to Categorizer Rules. Fill out some typical rules (Deposit -> Sales Revenue) and save. 
5. Now go to Reconciliation, and use the demo data that's stored on [this confluence page](https://benchco.atlassian.net/wiki/spaces/BAS/pages/2958590348/Misc.+Resources) to upload transactions for the test accounts. If you do not have access to that page, ask BAS.
6. Post the transactions when you're done. Now go to the Review tool, select the year and do a self review. You can do this by flipping every field to 'No Errors Found'. Once you've done that, you'll need to do it again but this time, complete it as a monthly **peer** review. 
7. Now go to Flo and flip the months with outstanding categorizations to 'REQ', and send a touchpoint that includes a categorizer link. 
