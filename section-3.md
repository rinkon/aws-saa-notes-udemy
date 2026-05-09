### Section 3

##### Regions & Availability Zones
- Worldwide regions 39 (example: ap-southeast-2 which is in Sydney)
- Worldwide Availability Zones 123 (example: ap-southeast-2a, ap-southeast-2b, ap-southeast-2a)
- One Region can have minimum 3 and maximum 6 AZ
- 400+ Points of presense. 400+ edge locations (like CDNs), 10+ Regional Caches

```
User → Edge Location → Regional Edge Cache → Origin Server.
```

---
How to choose an AWS Region:
1. Compliance
2. Proximity
3. Availability (New services might not be available to all regions)
4. Pricing
---
Most services are region-scoped except these Global Services:
1. IAM
2. Route 53
3. CloudFront
4. WAF (Web Application Firewall)
