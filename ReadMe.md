## Ticketbooth API
## Tech Stack
- NodeJs
- SQLite3
- Express
- EJS
- Node-fetch

## Big Picture
**Ticket Booth API** is an API server that is a digital ticket store 

## Summary of all the endpoints with examples
**GET REQUEST**

***Home Route -- Display a Welcome page saying Welcome to Ticket-Booth API***
```
GET "/" 
```
***All Events -- Display all the events created from the events table in the Database***
```
GET "/all_events"
```
***Participants Route -- Display all the participants from the participants table in the Database***
```
GET "/participants" 
```
***Tickets Route -- Display all tickets from the tickets table in the Database***
```
GET "/tickets"
```
***Admin Route -- Display all the admin from the admin table in the Database***
```
GET "/admin"
```
***Event Route -- Display event base on the id passed from the events table in the Database***
```
GET "/event/:id"
```
***Specific Ticket Route -- Display ticket base on the id passed from the tickets table in the Database***
```
GET "/ticket/:id"
```
***Ticket info -- Display ticket base on the id passed from the tickets table in the Database***
```
GET "/ticket_info/:event_name"
```
***Get Collection Route -- Getting collection from the Ponitor's API; Getting information about the mobile money transaction.***
```
GET "/get_collection"
```

## POST REQUEST
***Events Route -- Create new event and store it in the events table in the Database.***
```
POST "/events"
```
Format to use:
```js
{
	"event_name": "ODC",
	"currency": "LRD",
	"event_description": "This is tech event",
	"ticket_price": "500",
	"orange_account": "077777777" - NA,
	"lonestar_account": "08888888",
	"location": "Orange Digital Center",
	"event_date": "May 1, 2022",
	"num_participants": "109" - Optional,
	"status": "Confirm" -Optional,
	"img": "odc.url"
} 
```
***Admin Route -- Intend to use KeyCloak for authentication and store the register admin in the admin table.***
```
POST "/admin" 
```
***Tickets Route -- Make a call to the Ponitor's API to make the mobile money transaction to purchase a ticket and store the data in the tickets table in the Database.***
```
POST "/tickets"
```
Format to use:
```js
{
    "amount": "5",
    "msisdn": "231881524524",
    "currency": "lrd",
    "external_id": "09945",
    "message": "Ticket Booth ticket purchase.",
    "name": "Albin N, Karmo",
    "address": "Monrovia",
    "status": "Pending",
    "event_name": "My Event",
    "transaction_date": "03/1/2022"
}
```
## Project Installation and Configuration
### Installation: We have a package.json file already. Run the below command in your terminal
- npm install
### Run program
- npm start