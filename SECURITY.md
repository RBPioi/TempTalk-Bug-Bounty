# TempTalk Bug Bounty Program Rules
At TempTalk, the security of our users and their data is paramount. We invite security researchers to responsibly disclose vulnerabilities in TempTalk so that we can address them promptly. This program rewards responsible disclosures that help us identify and resolve security vulnerabilities in our application and website. Please read the rules below carefully to ensure your submissions qualify.

# Program Scope
The TempTalk Bug Bounty Program is limited to the latest versions of TempTalk on the following platforms:

- iOS (standalone app)
- Android (standalone app)
- PC application (Electron-based)
- *.temptalk.app
- *.chative.com
- *.chative.im

Note: Any submission regarding platforms not listed above, including other unsupported environments, is out of scope and will not be eligible for rewards.

# In-Scope Vulnerabilities

We welcome reports on the following types of vulnerabilities, each of which is eligible for reward:

1. Authentication and Authorization Issues 
·	Any weaknesses that could bypass or circumvent TempTalk’s login, signup, or account recovery mechanisms.
·	Issues that allow unauthorized access to user accounts or privileged sections of the application.
·	OAuth vulnerabilities, if applicable, that allow token theft, manipulation, or unauthorized account access.

2. Data Privacy and Confidentiality Vulnerabilities
·	Issues that expose or allow unauthorized access to user data, such as messages, media files, or personal information.
·	Any flaws that leak metadata (e.g., user status, online presence) beyond the intended privacy settings.
·	Misconfigurations or weaknesses in file storage that allow unauthorized access to user-generated files (e.g., photos, videos) either on the device or the server.

3. Account Takeover and Session Management Issues
·	Vulnerabilities that allow unauthorized parties to take over, hijack, or impersonate user accounts.
·	Session management flaws, such as insecure session tokens, session fixation, or insufficient session invalidation after logout.

4. Encryption and Cryptographic Weaknesses
·	Weaknesses in cryptographic protocols or algorithms used in messaging, file sharing, or user data encryption.
·	Man-in-the-Middle (MitM) attack possibilities due to insufficient TLS/SSL configuration or certificate validation.
·	Improper key management or weak cryptographic practices that could lead to data exposure or message interception.

5. Remote Code Execution (RCE) and Arbitrary Code Execution
·	Any vulnerability allowing attackers to execute unauthorized code on the user’s device or within the Electron-based PC application’s context.
·	Injection vulnerabilities within the Electron app (e.g., vulnerabilities in preload scripts) that may lead to RCE or unauthorized access.

6. Injection Attacks (e.g., SQL, NoSQL, or Script Injection)
·	SQL, NoSQL, or script injection vulnerabilities that could affect app functionality, data integrity, or data confidentiality.
·	JavaScript injection vulnerabilities specific to Electron (e.g., Cross-Site Scripting (XSS) within the app context) that could lead to information leakage or other impacts.

# Out-of-Scope Vulnerabilities

To keep our focus on the most impactful security issues, the following are considered out of scope and will not be eligible for rewards:

- Reports for Unsupported Platforms or Environments: Any issues on platforms outside iOS, Android, and the Electron-based PC app.
- Physical Access Requirements: Vulnerabilities that require physical access to the device to exploit.
- Social Engineering Attacks: Social engineering (e.g., phishing) against TempTalk users, employees, or support staff is not permitted.
- Issues in Third-Party Components or Services: Any bugs in third-party services that TempTalk does not directly control (e.g., cloud provider infrastructure).
- Denial-of-Service (DoS) Attacks: Attacks that disrupt service availability, including resource exhaustion or brute-force attacks against login pages.
- Outdated Version Reports: Any bugs found in outdated or unsupported versions of the TempTalk application.
- ser Experience or User Interface Bugs: Visual or functional bugs that do not directly affect security.

# Responsible Disclosure Policy

We ask all security researchers to adhere to responsible disclosure principles:

- No Public Disclosure: Please avoid publicly sharing or discussing the vulnerability until TempTalk has verified and addressed it.
- Use Only Your Test Accounts: Do not access, alter, or damage data belonging to TempTalk users.
- Limit Your Impact: Conduct testing in a way that does not disrupt the TempTalk service for other users.

Failure to adhere to these policies may result in disqualification from the bug bounty program and a ban from future participation.

# Reporting Procedure

To ensure we can verify and triage your findings efficiently, please submit vulnerability reports via email to [security@chative.com](mailto:security@chative.com) with the following details:

1. Clear Title and Description
Provide a concise title (e.g., "Session Fixation Vulnerability in iOS TempTalk App") and a detailed description of the issue.
2. Proof of Concept (PoC)
Include detailed steps to reproduce the issue, along with a proof-of-concept (PoC) that may include screenshots, videos, code samples, or logs.
3. Platform and Version Information
Specify the TempTalk app version and the operating system (iOS, Android, or Electron-based PC) where you found the vulnerability.
4. Impact Assessment
Clearly outline the security impact of the vulnerability and explain any potential risks to users or data.
5. Any Supporting Materials
Attach any scripts, payloads, or files that may help us replicate the issue on our end.

Submissions that are incomplete or vague may result in delayed evaluation or disqualification from rewards.

**Note: To ensure that the vulnerability you found is not stolen during transmission, please fill in the vulnerability details in a PDF document and encrypt it with a key. You can briefly summarize the vulnerability type and impact in the body of the email, but do not describe the vulnerability details in the body of the email.**

Please use the public key below to encrypt the PDF file, and then add the encrypted PDF file to the attachment and send it to the TempTalk mailbox[security@chative.com](mailto:security@chative.com).
Obtain the public key file security.gpg. Import the public key into your GPG keyring:
gpg --import security.gpg
Encrypt the file using the public key:
gpg --encrypt --recipient "security@chative.com” filename
This will produce an encrypted file (e.g., filename.gpg) that you can send to the security@chative.com

PGP PUBLIC KEY：https://raw.githubusercontent.com/RBPioi/sec/refs/heads/main/security.gpg

# Reward Criteria

Rewards are determined based on the impact, risk level, quality, and clarity of the report. All reward decisions are final and are assessed according to the following general criteria:

- Critical: Vulnerabilities with immediate risk of large-scale exploitation, such as RCE, significant data breaches, or account takeover on a mass scale.
- High: Issues that can lead to unauthorized access, unauthorized data exposure, or control of a single user account.
- Medium: Moderate vulnerabilities affecting a subset of users or requiring complex exploitation methods.
- Low: Minor issues with limited exploitability or impact, often requiring significant user interaction to exploit.

Rewards are assessed individually based on severity, with higher payouts for clear, reproducible, and impactful reports.


# Legal Safe Harbor

TempTalk pledges to not pursue legal action against researchers who report security vulnerabilities in good faith and adhere to these rules. Testing that breaches these boundaries or significantly disrupts TempTalk’s services may result in legal action and disqualification from this and future programs.

# FAQ

**Q: Can I disclose the vulnerability publicly once I report it?**

A: No, please wait until we confirm that the vulnerability has been resolved. We will notify you when it is safe to disclose your findings.

**Q: How long does it take for reports to be reviewed?**

A: We strive to acknowledge your submission within 72 hours. Evaluation and resolution times will vary based on severity and complexity.

**Q: What happens if I submit multiple vulnerabilities?**

A: Each unique, in-scope vulnerability is eligible for an individual reward. Submissions of duplicate or similar issues may not be eligible for additional rewards.

**Q: Who do I contact if I have questions about these rules?**

A: Feel free to reach out to our team at [security@chative.com](mailto:security@chative.com) for any clarifications or questions regarding the program. You can also join the [TempTalk discord group](https://discord.gg/9sYV6AUk) to see the latest announcements


Thank you for helping make TempTalk a secure platform for everyone. We look forward to your contributions and appreciate your efforts to responsibly disclose any vulnerabilities you find. Happy hunting!
