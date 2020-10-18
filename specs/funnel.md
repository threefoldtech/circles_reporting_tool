# funnel

- name starts with FUNNEL_
- is to track business opportunities

## custom fields

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
  part: 10%
  type: booking
- 
  user: despiegk
  part: 30%
  type: revenue
  
```

- part is the percentage of the deal in booking or in revenue (revenue means as money came in from the customer)
- type: revenue or booking, if not specified is revenue
- user: name as defined in [user](user.md), needs to exist in this instance of the tool
- rest of fields see in bookings 



