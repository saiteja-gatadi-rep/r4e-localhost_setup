# Actions in NOVA reporting (mobile copy, diagrams as images)

Stories: ACT-5460 (Actions data source), ACT-5461 (P0 reports), ACT-5469 (report library). Epic ACT-5278.

## 1. What is this
Actions (tickets) is now the fifth data source in NOVA Dashboards & Reports, turned on per tenant with one feature flag.

![diagram 1](images/d1.png)

## 2. Why NOVA
One self-serve engine, builder and library for every source, instead of a separate fixed set of ticket reports.

![diagram 2](images/d2.png)

## 3. How it helps
Ticket numbers become self-serve dashboards next to Reviews and the other sources.

![diagram 3](images/d3.png)

What the source offers:
![diagram 4](images/d4.png)

## 4. Who sees it
Three switches, all per tenant.

![diagram 5](images/d5.png)

## 5. How it works
The report engine offers Actions only when the switches are on; the report library lists Actions dashboards only for flagged tenants.

![diagram 6](images/d6.png)

## 6. Where the ticket data comes from
Tickets flow into the Elasticsearch index through the pipeline; NOVA only reads the index. On QA the pipeline is not live yet, so the index has a few hand-loaded test tickets.

![diagram 7](images/d7.png)

## 7. What we are covering
Everything runs on localhost against real QA data: tenant 1286, the saved dashboard "Actions-Demo", date = Calendar Year 2023.

![diagram 8](images/d8.png)

## 8. Status
Known engine issue below = group by plus metric sort returns a 500 from Elasticsearch; same on Reviews.

![diagram 9](images/d9.png)

## 9. Points to be noted
![diagram 10](images/d10.png)

Suggestions from PMs:
- 
- 
- 

## 10. Real vs dummy data
Real ticket, real index, real report service code. Test-only: the flag and module on QA tenant 1286, and the backend on localhost instead of QA.

![diagram 11](images/d11.png)
