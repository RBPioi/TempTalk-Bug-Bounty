# TempTalk Bug Bounty Program

TempTalk welcomes developers and the security research community to audit its services, code and protocol seeking vulnerabilities or security-related issues.

Security researchers can submit any relevant issues they find at security@chative.com All reports submitted in accordance with the rules and scope outlined below which result in a change of code or configuration are eligible for bounties, ranging from $100 to $100,000 or more, depending on the severity of the issue.

> TempTalk's bug bounty program has been continuously active since 2024.

### Rules and Principles

Generally speaking, the purpose of TempTalk's bug bounty program is to improve the safety of our platform thanks to cutting-edge technologies and modern penetration testing techniques. In accordance with this principle, we expect security professionals to employ common sense and to operate in good faith when researching issues – below is a non-exhaustive list of rules that always apply:

- Your testing cannot violate any law, disrupt TempTalk's services or negatively affect other users in any way.
- Vulnerabilities that are disclosed to the public or to third parties before they are addressed are not eligible for our bug bounty program. This includes vulnerability brokers.
- Attempting to gain physical access to any of TempTalk’s equipment is strictly prohibited.
- Should you be eligible for a prize, you are responsible for any taxes and fees depending on your country of residency.
- This bounty program is security-focused and therefore does not cover denial of service or load balancing issues resulting from spam, brute forcing, coordinated DDoS attacks, etc. Consequently, you are not allowed to perform any such action on our services.

Researchers are welcome to use our dedicated test environment if they require it – instructions on how to access it can be found here.

> TempTalk will not take legal action against anyone who responsibly researches and discloses vulnerabilities in accordance with our rules.

### Non-qualifying issues

Reports should focus on the security-related severity and impact of the vulnerability. Below is a non-exhaustive list of issues that generally do not qualify for our program.

1. Phishing attacks, spam
2. Token or session hijacking as a result of external malware on the OS
3. Irrelevant reports from scanners or automated tools
4. Attacks requiring physical access to the user's device
5. Missing cookie flags (HttpOnly, Secure, etc.)
6. Attacks requiring root access to the user's device
7. Clickjacking
8. Non-reproducible vulnerabilities deriving from outdated or reportedly flawed versions of open-source software
9. Vulnerabilities that rely on social engineering to either obtain sensitive credentials or have the user perform an unlikely sequence of actions
10. Presence of banner or version information, SSL/TLS best practices, etc.

> An issue may only be submitted once. Duplicate issues submitted by either the same person or multiple people do not qualify – only the first report will be evaluated.

### Program Scope

Generally, any TempTalk-owned or operated app, web service, domain, server and protocol that either handles or stores private user data is in scope.

Any unrelated bug (e.g. usability, interface, etc.) that doesn't impact security in any way is out of scope and should instead be reported on our dedicated public bug tracking platform.

~#### Protocol~

~TempTalk relies on MTProto 2.0, a protocol specifically designed for speed and security. The full technical documentation is available here. We welcome any reports about vulnerabilities or design flaws in the protocol which could realistically result in unauthorized access to user data.~

#### Applications

Official TempTalk apps are open source and support reproducible builds. Pre-built executables can be found here, while the full source code for each app is available here.

#### Domains

Below is a list of TempTalk domains which can be considered in scope. Third-party domains that integrate TempTalk pages or services are out of scope. Low-impact issues which don't pose a significant risk and don't fall under our non-qualifying issues may be in scope but could be awarded a smaller prize.

- iOS (standalone app)
- Android (standalone app)
- PC application (Electron-based)
- *.temptalk.app
- *.chative.com
- *.chative.im

#### Third-Party Applications and Services

Apps developed by third parties using the open TempTalk API, as well as bots running under TempTalk's Bot API, can only be considered in scope if the report targets a vulnerability on our end (e.g. vulnerable endpoint which poses a security risk).

Issues caused by third-party developers' malpractice, negligence or incorrect implementation of our Security Guidelines are out of scope and should instead be promptly reported to the relevant developers.

### Submission

If you found an issue which is in scope, is eligible and was found in accordance to our rules, you are welcome to submit it to security@chative.com.

We expect all reports to be written in English and to follow a consistent template, spacing included:

```
# Attack surface: (e.g. my.TempTalk.org/auth)
# Severity: (e.g. 7) [Optional, CVSS v3 rating]

## Description: 
[Describe the vulnerability briefly here, including its type]

## Steps to reproduce:
[1] Step one...
[2] Step two...
[n] Finally...

## Impact:
[What practical, realistic risk does this vulnerability pose?]

## Additional details:
[Tools used, preconditions, media proof, session and timestamps as needed]
```

##### Third-Party Bug Bounty Platforms

We ask for all submissions and correspondence to be sent directly to security@chative.com – TempTalk currently does not maintain a presence on third-party bug bounty platforms or services.

### Prize

Valid reports that result in a change of code or configuration are eligible for bounties, ranging from $100 to $100,000 or more, depending on the severity of the issue. We reserve the right to ultimately determine both the validity and the appropriate compensation for each report at our discretion.

> In general, app-level changes can expect bounties ranging from $100 to $10,000. Protocol-level issues may be eligible for rewards of up to $100,000 or more.

~#### Test Environment~

~To log in to the test environment, use either of the following:~

~iOS: tap 10 times on the Settings icon > Accounts > Login to another account > Test.~
~TempTalk Desktop: open ☰ Settings > Shift + Alt + Right click ‘Add Account’ and select ‘Test Server’.~
~macOS: click the Settings icon 10 times to open the Debug Menu, ⌘ + click ‘Add Account’ and log in via phone number.~

~The test environment is completely separate from the main environment, so you will need to create a new user account (or a new bot with @BotFather).~

~You can send requests to the test Bot API in this format:~

~`https://api.temptalk.com/bot<token>/test/METHOD_NAME`~

~> When working within the test environment, you may use HTTP links without TLS to test Web Apps.~

