# commons-security-risk
1. Problem statement: APIs are vulnerable to brute-force attacks, credential stuffing, and volumetric abuse without a centralized, pluggable rate-limiting and threat-scoring framework.

2. Concepts and terminology: Token Bucket Algorithm, Sliding Window Rate Limiting, Threat Scoring, Request Sanitization.

3. Available technologies / algorithms: Redis (Lua scripts for atomic token buckets), Bucket4j, Spring Interceptors.

4. When to use what: Use at the API gateway or entry filter layer to throttle abusive traffic and flag suspicious behavioral patterns.

5. Java APIs and dependencies: Bucket4j-redis, Spring Data Redis, Jakarta Servlet API.

6. AWS equivalents: AWS WAF, Amazon API Gateway Rate Limiting.

7. Architecture patterns: Edge Rate Limiting, Token Bucket Pattern, Circuit Breaker Fallbacks for Rate Limits.

8. Security considerations: Ensure rate-limiting keys are hashed (e.g., hashed client IPs) to comply with data privacy regulations.

9. Implementation examples: Servlet filter enforcing IP/User-based rate limits using Redis reactive counters.

10. References and further reading: OWASP API Security Top 10 (API4: Unrestricted Resource Consumption).
