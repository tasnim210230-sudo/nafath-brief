Version: NAFATH-V1
Track: Software

## Overview
NAFATH is a national digital login service that allows citizens to access different government services using one account. Six IT fields work together to make the service secure and reliable. Software manages authentication and delegated access. AI can help detect suspicious login activity. Mobile development controls application permissions. Networking protects communication such as DNS requests. Cybersecurity strengthens authentication and reduces phishing risks. Data management protects citizens’ personal information and supports compliance with Oman’s Personal Data Protection Law. Together, these six fields help create a secure, accessible, and trustworthy digital identity service for citizens.
## Software
OAuth 2.0 and OpenID Connect have different purposes. OAuth 2.0 is mainly used for authorization, which means allowing an application to access approved resources on behalf of a user. OpenID Connect is used for authentication, which means confirming the user’s identity during login. OpenID Connect is built on top of OAuth 2.0 and adds identity information, such as an ID token, for secure sign-in.
Resource: How OpenID Connect Works – https://openid.net/foundation/how-connect-works/
## AI
Before using AI to flag suspicious logins, the authority should manage risks such as false positives, missed attacks, privacy concerns, security weaknesses, bias, and poor explainability. The NIST AI Risk Management Framework recommends that AI systems be valid and reliable, safe, secure and resilient, accountable and transparent, explainable, privacy-enhanced, and fair. These risks should be tested, measured, monitored, and managed before and after deployment.
Resource: Artificial Intelligence Risk Management Framework (AI RMF 1.0) – https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-1.pdf
## Mobile
Android limits access to sensitive data and device features through permissions. Runtime permissions, also called dangerous permissions, are required for actions such as using the camera, microphone, contacts, or location. The app should request permission only when the user starts a feature that needs it, not automatically at startup. If permission is denied, the app should continue working where possible without that restricted feature.
Resource: Permissions on Android – https://developer.android.com/guide/topics/permissions/overview
## Networking
DNS over HTTPS (DoH) sends DNS queries through an encrypted HTTPS connection instead of sending them in plain text. This helps protect users from people on the network seeing or changing their DNS requests. However, DoH does not hide all internet activity. Websites can still see connections, and other traffic information may still be visible. It mainly protects DNS queries, not the entire connection.
Resource: RFC 8484 - DNS Queries over HTTPS (DoH) – https://www.rfc-editor.org/rfc/rfc8484
## Cybersecurity
Phishing-resistant authentication prevents users from giving an attacker a reusable login secret. Methods based on FIDO2 or WebAuthn are phishing-resistant because they use cryptographic credentials linked to the real website. SMS codes, email codes, and one-time passwords are not phishing-resistant because attackers can trick users into entering them on a fake site and use them immediately.
Resource: NIST Special Publication 800-63B – Digital Identity Guidelines: Authentication and Lifecycle Management – https://pages.nist.gov/800-63-4/sp800-63b.html
## Data
Under Oman’s Personal Data Protection Law, the authority must protect citizens’ personal data and process it lawfully. It should obtain consent when required, clearly explain why the data is collected, protect its confidentiality, keep processing records, respect users’ rights to access or correct their data, and report certain data breaches. Appropriate technical and organizational measures must also be used to reduce privacy and security risks.
Resource: Personal Data Protection – Ministry of Transport, Communications and Information Technology – https://www.mtcit.gov.om/sectors/governance/personal
## Misconception in My Track
A common misconception is that OAuth 2.0 and OpenID Connect do the same job. OAuth 2.0 mainly provides a framework for authorization and access to resources, while OpenID Connect adds an identity layer that supports user authentication and login. The OpenID Foundation explains this under the section “What is OAuth 2.0 and how does it related to OpenID Connect?” This distinction is important because a login service must verify who the user is, not only what resources an application may access.
## Open Question
How should NAFATH securely manage user sessions and token expiration across multiple government services without forcing users to log in repeatedly?
