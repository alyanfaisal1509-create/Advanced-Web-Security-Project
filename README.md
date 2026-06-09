# Cybersecurity Internship - Weekly Progress Report

This repository documents the weekly progress of my Cybersecurity Internship, focusing on securing a web application using modern security practices, ethical hacking, and compliance with OWASP guidelines.

---

## Table of Contents

- [Week 4: Advanced Security Mechanisms & Threat Monitoring](#week-4-advanced-security-mechanisms--threat-monitoring)
- [Week 5: Ethical Hacking, Vulnerability Testing & CSRF Protection](#week-5-ethical-hacking-vulnerability-testing--csrf-protection)
- [Week 6: Final Security Audit & OWASP Compliance](#week-6-final-security-audit--owasp-compliance)
- [Security Features Summary](#security-features-summary)
- [Technologies Used](#technologies-used)

---

## Week 4: Advanced Security Mechanisms & Threat Monitoring

### Objective
The objective of Week 4 was to improve application security using advanced web security mechanisms and threat monitoring.

### Tasks Performed

#### 1. Rate Limiting Implementation
- Implemented rate limiting using the `express-rate-limit` middleware.
- **Result:** Restricted excessive requests to prevent brute-force attacks. Multiple repeated requests were successfully blocked after the request limit was reached.

#### 2. Security Headers Enhancement
- Configured `Helmet.js` middleware for improved HTTP security headers.
- Implemented Content Security Policy (CSP) configuration.
- Enabled HTTP Strict Transport Security (HSTS).
- **Result:** Browser security policies were strengthened against common web vulnerabilities.

#### 3. Failed Login Monitoring
- Implemented failed login attempt logging using Winston.
- Suspicious authentication attempts are now stored in the application logs.
- **Result:** Unauthorized login attempts can now be monitored and analyzed.

#### 4. Logging & Monitoring
Security-related events such as the following are now continuously logged:
- User login
- User registration
- Failed login attempts
- Server activity

### Security Features Implemented (Week 4)
- Rate Limiting
- Helmet.js Security Headers
- CSP Configuration
- HSTS Protection
- Failed Login Monitoring
- Winston Logging

### Conclusion
Week 4 successfully enhanced the web application security by implementing brute-force protection, monitoring mechanisms, and secure HTTP security headers.

---

## Week 5: Ethical Hacking, Vulnerability Testing & CSRF Protection

### Objective
The objective of Week 5 was to perform ethical hacking activities, test common web vulnerabilities, and implement CSRF protection.

### Tasks Performed

#### 1. Ethical Hacking & Vulnerability Testing
- Performed manual vulnerability testing on authentication forms and input fields.
- Tested application behavior against common web vulnerabilities.

#### 2. SQL Injection Testing
- Conducted manual SQL Injection testing on login forms.
- **Result:** Since the application uses MongoDB (NoSQL database), traditional SQL Injection vulnerabilities were not applicable. No injection vulnerability was found.

#### 3. CSRF Protection
- Implemented CSRF protection using the `csurf` middleware.
- Configured `cookie-parser` for secure token handling.
- **Result:** Unauthorized and forged requests are now protected using CSRF tokens.

#### 4. Security Validation
- Verified secure middleware configuration.
- Confirmed application stability after implementing security features.

### Security Features Implemented (Week 5)
- CSRF Middleware
- Cookie Parsing Security
- Authentication Testing
- Injection Testing

### Conclusion
Week 5 successfully implemented ethical hacking practices and CSRF protection to improve the application's resistance against unauthorized requests.

---

## Week 6: Final Security Audit & OWASP Compliance

### Objective
The objective of Week 6 was to conduct a final security audit, review compliance with OWASP security practices, and prepare the application for secure deployment.

### Tasks Performed

#### 1. Security Audit
- Reviewed all implemented security features in the application.
- Verified authentication, validation, logging, and protection mechanisms.

#### 2. OWASP Top 10 Compliance Review

The application security was reviewed against common OWASP Top 10 vulnerabilities:

| OWASP Risk | Security Measure Implemented |
|------------|---------------------------|
| Broken Authentication | JWT Authentication & bcrypt |
| Injection Attacks | Input Validation |
| Security Misconfiguration | Helmet.js |
| Brute Force Attacks | Rate Limiting |
| CSRF Attacks | csurf Middleware |
| Insufficient Logging | Winston Logging |

#### 3. Secure Deployment Review
- Ensured sensitive environment variables are stored securely.
- Verified that secret files are excluded from GitHub (`.gitignore`).
- Reviewed dependency security and middleware configurations.

#### 4. Final Penetration Testing
Performed final testing on:
- Login system
- Signup validation
- Rate limiting
- CSRF protection
- Authentication security

### Final Security Features
- Password Hashing using bcrypt
- JWT Authentication
- Helmet.js Security Headers
- Rate Limiting
- CSRF Protection
- Winston Logging
- Input Validation

### Conclusion
Week 6 successfully completed the final security audit and deployment security review for the web application. The application now follows modern security practices and includes multiple layers of protection against common web threats.

---

## Security Features Summary

| Feature | Description | Week |
|---------|-------------|------|
| Rate Limiting | Prevents brute-force attacks by limiting request frequency | 4 |
| Helmet.js | Secures HTTP headers and configures CSP | 4 |
| HSTS Protection | Enforces HTTPS connections | 4 |
| Failed Login Monitoring | Logs suspicious authentication attempts | 4 |
| Winston Logging | Centralized logging for security events | 4 |
| CSRF Protection | Prevents cross-site request forgery attacks | 5 |
| Cookie Parsing Security | Secure token handling for sessions | 5 |
| SQL/NoSQL Injection Testing | Verified database input sanitization | 5 |
| JWT Authentication | Stateless token-based authentication | 6 |
| Password Hashing (bcrypt) | Secure password storage | 6 |
| Input Validation | Prevents malicious user input | 6 |
| Secure Deployment | Environment variable and secret management | 6 |

---

## Technologies Used

- **Node.js** - Runtime environment
- **Express.js** - Web application framework
- **MongoDB** - NoSQL database
- **bcrypt** - Password hashing
- **JWT (jsonwebtoken)** - Authentication tokens
- **Helmet.js** - HTTP security headers
- **express-rate-limit** - Rate limiting middleware
- **csurf** - CSRF protection middleware
- **cookie-parser** - Cookie parsing middleware
- **Winston** - Logging library
- **OWASP Top 10** - Security compliance framework

---

> **Note:** This internship focused on building a secure web application by implementing defense-in-depth strategies across multiple layers of the application stack.

