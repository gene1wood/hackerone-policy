Our rewards are based on the severity of the issue and the criticality of the service or application. The bounty table lists the range of bounties we pay for vulnerabilities in our applications and **does not apply on out of scope reports**.

The severity is calculated based on the impact of the vulnerability and the likelihood of finding and exploitating the vulnerability. Below are the definitions of each impact and likelihood level and some examples. Note that these lists are not extensive and the final severity decision is up to the discretion of Mozilla.

# Impact Definitions and Examples

## Critical

Critical vulnerabilities are urgent security issues that present an ongoing or immediate danger to the users of our services and our infrastructure

* Remote Code Execution with unauthenticated public internet access
* Authentication and Session Management Flaws (which lead to account compromise and takeover)
* Disclosure of secrets in publicly accessible assets
* Hardcoded credentials for a privileged user

**Note that Critical vulnerabilities found in out of scope assets are awarded in the range of $500-$1000.**

## High

 Typically, high severity issues are exploitable web vulnerabilities that can lead to the targeted compromise of a small number of users.

* Account takeover through Oauth misconfiguration
* IDORs that bypass authentication or authorization for significant actions
* CSRF on significant actions, such as changing email/passwords, deleting accounts, etc.
* XSS resulting in conducting significant action (i.e., not defacement, phishing, cookie injection, etc.)
* XML External Entity (XXE) attack
* Hardcoded credentials for a non-privileged user

## Medium

 Vulnerabilities which can provide an attacker additional information or positioning that could be used in combination with other vulnerabilities. In addition to issues resulting from the lack of standard defense in depth techniques and security controls.

* XSS (minor)
* Domain takeovers supported by a proof of concept for `*.mozilla.org`, `*.mozilla.com`, `*.mozilla.net`, `*.firefox.com`, `*.mozgcp.net` and `*.mozaws.net` in addition to the list of sites in scope (excluding staging instances). If the domain is pointing to a claimed instance by another company, then the report will not be eligible for bounty.
* SSRF which leads to reaching **internal** network hosts
* Disclosure of sensitive information which does not expose the user or organization to immediate risk
* CSRF for minor actions.

## Low

 Minor security vulnerabilities which could lead to leaks or spoofs of non-sensitive information. Missing best practice security controls

* XSS (blocked by CSP)
* Clickjacking with demonstrated impact (Lack of clickjacking protection (XFO, CSP) is insufficient to claim a bounty)
* External SSRF

**Note that some low severity issues are not eligible for monetary awards based on their impact.

# Likelihood Definitions and Examples

Below are some of the factors we take into consideration when determining the likelihood:

* Public internet access vs access from the internal network
* Authenticated vs unauthenticated access
* Required permissions and access level
* Required user interactions
* Attack complexity
* Mitigating security controls

## High

* The vulnerability can be exploited using unauthenticated public internet access
* The vulnerability can be exploited using an authenticated regular user without any special privileges
* Hard corded credentials in a publicly accessible resource

## Medium

* The vulnerability requires one user interaction to be exploited
* The vulnerability can be exploited using low level permissions which are provided to regular users

## Low

* The vulnerability can be exploited using admin access or high level permissions which are only given to specific users
* The vulnerability can be exploited using local device access
* The vulnerability requires multiple user interactions to be exploited
* The vulnerability is mitigated by WAF, CSP or other security controls
 

# Out of Scope

* We follow HackerOne's standard for [Core Ineligible Findings](https://docs.hackerone.com/en/articles/8494488-core-ineligible-findings).
* In addition to the [custom scope exclusions](https://hackerone.com/mozilla?type=team#scope_exclusions) listed on our policy page

# Misc Notes
We have a bug bounty panel whose members decide whether a report is eligible for bounty and the bounty amount for eligible reports. The panel meets on a weekly basis, except for holidays and vacations, to discuss bounty decisions.

Please note these are general guidelines, and reward decisions are up to the discretion of Mozilla.
