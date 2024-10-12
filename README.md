# Magento Technical Test

```
Name: Email:
```
# Notes:

```
● Code examples are not required unless specified in the question, but feel free to include brief code
examples for any of the questions.
● You are expected to add a brief explanation of any design patterns you propose in your answers / code,
and their pros and cons if applicable
```
# Question 1: (No Code Required)

A website would like to set up sms notifications based on various events on the system (Orders, Shipments,
ect)

```
● We will be connecting to an SMS gateway service over rest APIs, the core implementation should be
abstract enough to be easily replaceable between different providers/gateways
● We should be able to configure different sms message templates for different events, for example
○ Order created
○ Order cancelled
○ Shipment Created
○ Shipment tracking created / updated
● The sms message templates should support simple variables that will be parsed and filled on the final
message, for example
○ Customer name
○ Order Number
● We should be able to see a list of the sms messages that were sent and their status, and errors in case
of failure
● The solution proposed should support a large volume of transactions / messages per hour, Ex: 1k
messages per hour
```
Describe the structure of the solution that will accomplish the requirements with technical details on how you
will implement each of the required features.

# Question 2: ( Code Example )

A website would like to add a feature where they can show different “Eligible For Return” values per product

```
● The value should be stored on a product attribute, that takes numerical value (days)
● The value will be rendered on the product page, Ex: Eligible for Returns within 7 days of delivery.
● There should be a way to turn off the display of the return text on the frontend
● The return eligibility data should be exposed over GraphQL APIs, including any configurations
● No frontend related changes are required
```
You are expected to


```
● Provide an explanation of the implementation and any functional improvements that can be proposed
● Provide code implementation for the all the requirements
```
# Question 3: (Code Example)

A website would like to add a new address field to capture the customer’s area

```
● A new field called area should be added to the customeraddress entity
● The values in the field should be available in the customer shipping & billing address
● The values in the field should be persisted in the quote & order addresses
● The field should be exposed over Magento’s rest apis for (Customer & Customer Address, Order info)
● The field should be exposed over Magento’s graphql mutations for creating & updating the customer
address
● The field should be exposed over Magento’s graphql queries that return a customer / order address
```
You are expected to

```
● Provide an explanation of the feature implementation to cover all the requirements
● Provide code implementation for all the requirements
```
# Question 4: ( BriefCode Example )

A website would like to add a feature (Price Drop Notification) for products, where customers can opt-in for
notifications whenever the product price changes to a lower value

```
● We should be able to enable / disable the feature globally
● We should be able to enable / disable the feature for specific products
● Price drop notifications would be sent to the opted in customers via email
● The frontend for the feature is a headless React frontend that consumes GraphQL APIs
```
Bonus Features
● Customers should be able to opt out of notifications
● We should be able to configure price drop thresholds for triggering a notification, Ex: > 10%

You are expected to

```
● Provide an explanation of the feature implementation to cover all the requirements
● Provide details on how the data will be stored and processed for customers who opt in
● Provide details on how the notifications will be processed
● Provide details on how the feature might be handled for logged in vs logged out customers
● Provide details as well as Sample Code Implementation for all the related GraphQL (Queries /
Mutations)
```


