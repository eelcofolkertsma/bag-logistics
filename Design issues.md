Different views on the servers
1 each party hosts its own publications
2 airline hosts the publications

Option 1 is agnostic in ownership of baggage information. 
The focus is on message ownership

Option 2 can be justified from business roles: 
customer delivers bag in custody of airline. 
Airline secures confidentiality with handlers. 
This includes managing the broker where bag information is published

http pubsub pattern
- airline hosts information on a bag
- handler may request this information (GET)
- handler may add to bag nformation, e.g. bag is loaded (POST)
- to avoid high pulling volume on GET, handler may provide a callback url 
where airline POSTs notifications on information updates

airline endpoint is well advertised, behind authentication/authorization
handler notification endpoint is private
