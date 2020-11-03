# funnel

- name starts with FUNNEL_
- is to track business opportunities or strategic partners (its a commercial funnel)
- template is on https://circles.threefold.me/project/despiegk-template_funnel/admin/project-profile/details

## structure

- modules
  - kanban
  - issues
  - wiki
  
## how are the objects used to represent a funnel

- an issue = is an oportunity (1 specific object)
- once the status is to deal it goes to the kanban where it will be dealt with with more info, it means customer +- ready to sign

## statuses

### issue

- New
- Interested
- Deal
  - means moved to story
- Blocked
  - project/deal/lead cannot be continued, something is blocking it, important to unblock asap
- NeedInfo
  - e.g. send proposal, need to send message, ...
- Lost
- Postponed
- Won

### story (is a deal)

- New (means is a deal, we need to make a proposal, or customer said yes so we can continue)
- Proposal
- Contract
- Blocked
  - project/deal/lead cannot be continued, something is blocking it, important to unblock asap
- NeedInfo
  - e.g. send proposal, need to send message, ...
- Closed 
    - can be a project_ ... means we need to work on a bigger project with a customer
    - can be a signed, so nothing to do, make sure in comments field add link to customer home page


### item (is a task or checklist on the story)

- New
- In progress
- Verification
- Closed
- Needs info


## Serverities

the estimate chance to get to closure on the opportunity

- unknown
- low
- 25%
- 50%
- 75%
- 90%

## Priority

how urgent to work on the next step in the process

- Low
- Normal
- High

## custom fields

are only custom fields on issues & stories (are 100% alike) !

### bookings

```yaml
-
  period: month
  duration: 10
  amount: 1000
  currency: usd
  start_date: 
-
  amount: 1000
  start_date: 
  confidence: 50
```

- period is onetime, month or year, default onetime if not specified
- duration 1 till max 120 ( integer), nr of times it happens, std 1
- amount integer
- currency: usd, chf, eur, gbp, egp (make lower case when tool parses, remove spaces, and check it exists), default eur
- start_date: date to expect when the business starts
  - format of date: $MONTH:$YEAR examples or $MONTH (if month allone then is month of the year itself we are in)
    - 1:2015
    - 01:2015
    - 11 -> 11:2020
    - 13 -> error
    - 0 -> error    
- confidence: 100% is the default (10 -> 10%, can only be 0,10,20,30,40,50,60.70,80,90,100

### commission

```yaml
-
  user: despiegk
  period: month
  duration: 10
  amount: 1000
  currency: usd
  start_date: 
- 
  user: despiegk
  part: 1%
  type: booking
- 
  user: andreas
  part: 5%
  type: revenue
  
```

- part is the percentage of the deal in booking or in revenue (revenue means as money came in from the customer)
- type: revenue or booking, if not specified is revenue
- user: name as defined in [user](user.md), needs to exist in this instance of the tool
- rest of fields see in bookings 



