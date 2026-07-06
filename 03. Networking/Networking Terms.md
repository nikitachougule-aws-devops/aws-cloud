
| Service              | Purpose                                  |
| -------------------- | ---------------------------------------- |
| **VPC**              | Private network                          |
| **Subnet**           | Division of a VPC                        |
| **Internet Gateway** | Internet access for public subnets       |
| **NAT Gateway**      | Outbound internet for private subnets    |
| **Route Table**      | Directs network traffic                  |
| **Security Group**   | Instance-level firewall (Stateful)       |
| **Network ACL**      | Subnet-level firewall (Stateless)        |
| **Elastic IP**       | Static public IP address                 |
| **ELB**              | Distributes traffic across EC2 instances |
| **Route 53**         | DNS service                              |
| **CloudFront**       | Content delivery network (CDN)           |

---

## Easy Way to Remember

```text
Internet
    │
    ▼
Internet Gateway
    │
    ▼
Public Subnet
    │
 ┌──┴─────────────┐
 │                │
EC2            NAT Gateway
 │                │
 │                ▼
 │          Private Subnet
 │                │
 │              Database
 │
Route Table decides where traffic goes.
Security Group protects the EC2 instance.
Network ACL protects the entire subnet.
Elastic IP provides a fixed public IP.
```
