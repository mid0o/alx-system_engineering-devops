Postmortem: API Gateway Outage

Links
Detailed Postmortem Report (Google Docs): https://docs.google.com/document/d/1UO3nmoETh7ZG7PtqdaCbBAUsxAPkucV1u320ok_rl5U/edit?usp=sharing
Advanced funny Postmortem on Medium: https://medium.com/@mohamedev/firsttt-postmortem-how-a-typo-crashed-our-api-gateway-and-my-sanity-057670092afa

Summary
On March 1, 2025, a misconfiguration in the API gateway’s rate limiter caused a 3-hour 15-minute outage, blocking all user requests. The issue stemmed from an incorrect setting (max_requests = 0), leading to a 100% service failure.

Key Details
Duration: March 1, 2025, 8:00 PM – 11:15 PM UTC
Impact: All API requests were rejected, causing a complete outage.
Root Cause: A misconfigured rate limiter with an invalid request limit.
Resolution: Rolled back configuration, restarted services, and cleared caches.
Preventative Measures
Add validation checks for configuration changes.
Implement real-time monitoring for request failures.
Automate backups for critical configuration files.
