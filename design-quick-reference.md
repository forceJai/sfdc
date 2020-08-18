# Design Quick Reference
This table summarises the fundamental design limits and benchmarks that an architect should keep in mind when designing a solution on the Salesforce platform.

## Design Limits
| What                                           |         Limit           |           Per    |
| ---------------------------------------------- | ----------------------: | ---------------: |
| Customer Community Users                       | 10,000,000              | Org              |
| Customer Community Plus Users                  | 300,000                 | Org              |
| Partner Community Users                        | 300,000                 | Org              |
| Roles                                          | 1,000                   | Org              |
| Territories                                    | 1,000                   | Org              |
| Territory assignment rules                     | 15                      | Territory        |
| Groups                                         | 100,000                 | Org              |
| Account-Territory sharing rules                | 300                     | Org              |
| Owner-based sharing rules                      | 300                     | Object           |
| Criteria-based sharing rules                   | 50                      | Object           |
| Line of demarcation: LDV (lower)               | 2,000,000               | Object           |
| Line of demarcation: LDV (upper)               | 100,000,000             | Object           |
| Line of demarcation: Wave (commercial limit)   | 250,000,000             | Object           |
| Data Skews: max records owned                  | 10,000 records          | User             |
| Data Skews: max child records per parent       | 10,000 child records    | Parent record    |
| Number of mass emails                          | 1,000                   | Day              |
| Number of emails sent via Apex                 | 1,000                   | Day              |
| Number of emails sent via workflows            | 2,000,000               | Day              |
| Apex Callouts                                  | 100                     | Transaction      |
| Apex Callout Timeout                           | 120 seconds             | Transaction      |
| Knowledge articles                             | 50,000                  | Org              |
| Knowledge languages                            | 16                      | Org              |
| Knowledge article types                        | 100                     | Org              |
| Knowledge attachment size                      | 25 MB                   | Attachment       |
| CRM content libraries                          | 2,000                   | Org              |
| CRM content files                              | 2,000,000               | Org              |
| CRM content files per pack                     | 50                      | Content Pack     |
| CRM content files size (uploaded via REST)     | 2 GB                    | File             |
| CRM content files size (uploaded via SOAP)     | 38 MB                   | File             |
| Attachment size                                | 25 MB                   | File             |
| Chatter file size                              | 2 GB                    | File             |
| Document file size                             | 5 MB                    | File             |
| Max fields in a Skinny Table                   | 100                     | Skinny Table     |
| Concurrent API requests (less than 20s)        | Unlimited               | Org              |
| Concurrent API requests (more than 20s)        | 25                      | Org              |
| SOAP API max batch size                        | 2,000 records           | Batch            |
| REST API max batch size                        | 200 records             | Batch            |
| Bulk API max batch size                        | 10,000 records          | Batch            |
| Bulk API max jobs                              | 5,000 jobs              | Day              |
| Streaming API - max PushTopics                 | 100                     | Org              |
| Streaming API - topic subscribers              | 2,000                   | Topic            |
| Data Storage - Developer Sandbox               | 200 MB                  | Sandbox          |
| Data Storage - Developer Pro Sandbox           | 1 GB                    | Sandbox          |
| Data Storage - Partial Copy Sandbox            | 5 GB                    | Sandbox          |
| Data Storage - Full Copy Sandbox               | Unlimited               | Sandbox          |
| Standard indexes - threshold                   | 30% of records          | query            |
| Standard indexes - cutoff (index not used)     | 1,000,000 records       | query            |
| Custom indexes - threshold                     | 10% of records          | query            |
| Custom indexes - cutoff (index not used)       | 333,000 records         | query            |

## Limits by volume of users
| What                                           |         Quota           |           Per    |
| ---------------------------------------------- | ----------------------: | ---------------: |
| API calls                                      | 1,000 - 5,000           | User             |
| Data Storage (internal user)                   | 20 - 120 MB             | User             |
| Data Storage (external user)                   | 1 - 20 MB               | User             |
| File Storage                                   | 612 MB - 2GB            | User             |

## Benchmarks
| What                                           |         Benchmark       |           Per    |
| ---------------------------------------------- | ----------------------: | ---------------: |
| Total transactions                             | 4 billion               | Day              |
| Transactions per second                        | 1,000,000               | Second           |
| Transaction duration                           | <300 ms                 | Transaction      |
| SOAP/REST API throughput (Read)                | 10 million records      | Hour             |
| SOAP/REST API throughput (Write)               | 2 million records       | Hour             |
| Bulk API throughput (Read)                     | 60 million records      | Hour             |
| Bulk API throughput (Write)                    | 20 million records      | Hour             |
