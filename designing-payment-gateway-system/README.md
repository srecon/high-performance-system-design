---
title: "Payment gateway system"
date: 2023-11-28 15:39
categories: designing high load system
language: EN
references:
   - None
---
## System descriptions:

### Payment System
3rd party payment system likes PayPal, Globalpay 


### Payment gateway
A router between payment systems
Storing interval state of transactions, requests to Payment systems and choosing routes to make transactions based on Payment - Setting configuration
Storing credentials of currency wallets and payment system accounts
1. Endpoints:
   1. /payments
   2. /payouts

### Payment settings
Currencies
Payment Systems
Payment Methods
Account of payment systems
Currency wallet of payment system
Settings for payment routes(cascading, priorities, distribution strategy)
and linkage of all this master data)

1. Endpoints:
   1. /payment-methods
   2. /currencies
   3. /routes
...


### Transaction log
Representation layer - read model for transactions state
Storing projection of transactions

### Account 
Storing Account balances
Storing master data of transactions and place to change balance based on the transaction events happened

1. Endpoints:
	1. /payments
	2. /payouts
	3. /confirm|decline - confirm or decline - confirm possibility to pay out money for client

### API Gateway 
	


## Backend protocols:
1. Protocols: RSocket, GraphQL, REST
2. Service Intercommunications: Service Mesh, RSocket Broker
3. Patters:
	1. Event Sourcing
	2. CQRS
	3. SAGA
4. Frameworks:
	1. Quarkus
	2. Spring boot
5. @todo

## Messaging 
1. Event Bus: Apache Pulsar

## Frontend stacks:
1. ReactJS
2. Protocols: REST, Asynch (kafka)
2. Identification/SSO etc. KeyCloack
3. API Gateway. 

## Datalake
1. Hadoop
2. Cassandra 

	
	
![Payment gateway highlevel view](payment-gateway-2.png)