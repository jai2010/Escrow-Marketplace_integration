# Integrate Secure Escrow Payments in a Online Marketplace

## Overview

Payoneer Escrow APIs makes it easy to integrate secure escrow payments into a marketplace. In this section, you'll see how to:

* Get a simple marketplace integrated with Payoneer Escrow API & enable secure escrow payments to their buyers & sellers.
* Take more control of the user experience.

## Scenario 
Your marketplace is focused on buying and selling electronic goods. Sellers register with your site and list items for sale. Buyers search and browse, and reach out to your sellers for quotation & the purchase (payment) of items happen outside your website. 

You are considering offering payment capability in your marketplace for your buyers and sellers to manage end to end purchase process. Criteria’s important for you to enable payments on your website are…

* Secure escrow payments to eliminate the risk of fraud 
* Licensed payment provider to process & hold payments safely
* Track shipments 
* Handle dispute between buyer & seller
* Transfer payments quickly to seller

All in all, you want a service provider who can help you with offering a simple & secure escrow payment service to users on your marketplace while you focus on offering the best user experience to your users.

## Simple Approach
To get up and running quickly, you decide that for your first version you'll leverage the Payoneer Escrow user interface as much as possible.

### Seller setup
You will have to create an account for your seller & also setup their payout preference on Payoneer before they can participate in an escrow transaction. During account creation, Payoneer conducts a comprehensive KYC check before approving the user to use escrow. We recommend you to add seller escrow setup to your onboarding process to eliminate RISKY sellers on your marketplace by leveraging our KYC checks for account approval.

#### Create a seller account
You can POST the partner details to accounts resource in Payoneer escrow API set to create an account for the seller. This also creates a user for that account. 

As part of account creation, we perform comprehensive KYC check on the user before enabling escrow for the user. KYC process involves checking the user against OFAC sanctioned list, etc…. [jai to update]
URI: /accounts

Parameters:
Type
Parameter
Required?
Description
string
company
optional
The name of the company (will use the user_name if none supplied)
string
user_name
required
The name of a contact at the company
string
user_email
required
The contact's email address
string
user_phone
required
The contact's phone number. Formatted with a plus sign, followed by the international dialing code, followed by a space, followed by the phone number (e.g. "+1 5551234567")
string
address
required
The company mailing street address
string
city
required
The mailing address city
string
state
required
The mailing address state/province (for US and Canadian addresses, use the 2-letter abbreviation for the state/province)
string
postal code
required
The mailing address zip/postal code
string
country
required
The mailing address country (2-letter ISO country code)
bool
email confirmed
optional
Has the user email address already been confirmed?
bool
agreed terms
optional
Has the user agreed to the Armor Payments terms and conditions?
What is the difference between account & user?
•	Account represents a company. Learn more
•	User represents a person at that company. Learn more

Now that you have created an account for the seller, you can setup the seller to enable escrow & also their payout preference.
Seller: Enable escrow & setup payout preference
