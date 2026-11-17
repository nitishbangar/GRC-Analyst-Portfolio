# MapleCloud Technologies Inc. – GRC Company Profile

Prepared by: Nitish Bangar, Junior GRC Analyst

16 November 2026

*Note: MapleCloud is a fictional company created for portfolio
practice.*

## 1. Company Overview

MapleCloud Technologies Inc. is a Software-as-a-Service (SaaS) company
based in Fredericton, New Brunswick. Founded in 2018, it provides a
cloud-based application that helps small businesses send invoices and
book appointments. The company has 71 employees. Some work from home,
while most work from the office daily. It serves about 1,200 business
customers across Canada, including some in Quebec.

MapleCloud is growing and is currently working to sign its largest
customer to date, a regional credit union. Before signing, the credit
union requires a SOC 2 report and a Software Bill of Materials (SBOM) to
confirm that MapleCloud protects customer data and manages its software
supply chain properly. MapleCloud has no formal security or compliance
program yet, so it has hired a Junior GRC Analyst to build one and
prepare the company for SOC 2. This will help MapleCloud win larger
customers and grow its security team in the future.

## 2. Business Operations

MapleCloud operates from its office in Fredericton, with some employees
working remotely. The company relies on several cloud services to run
its business. Its application is hosted on Amazon Web Services (AWS) in
the Canada region. Staff use Microsoft 365 for email, Teams and file
storage. Source code is stored on GitHub, payments are processed through
Stripe, and customer records are managed in Salesforce.

Because these services are provided by outside vendors, MapleCloud
depends on third parties to keep its data secure and its services
available.

The company is organized into the following teams:

| **Team**                 | **Staff** |
|--------------------------|-----------|
| CEO and CTO              | 2         |
| Engineering              | 30        |
| Sales/Marketing          | 15        |
| Customer Support         | 15        |
| Finance/HR               | 5         |
| IT                       | 3         |
| GRC (Junior GRC Analyst) | 1         |
| **Total**                | **71**    |

## 3. Information Assets

MapleCloud handles several types of sensitive information. Each asset is
listed below with where it is stored, its owner, its classification and
its most important security goal.

| **Asset**                                | **Where it's stored**         | **Owner**       | **Classification** | **Most important (CIA)** |
|------------------------------------------|-------------------------------|-----------------|--------------------|--------------------------|
| Customer data (names, emails, addresses) | Salesforce, AWS               | Head of Sales   | Confidential       | Confidentiality          |
| Customer invoices                        | AWS (app database)            | CTO             | Confidential       | Integrity                |
| Payment information                      | Stripe                        | Finance Manager | Restricted         | Confidentiality          |
| Employee HR and payroll records          | Microsoft 365                 | HR Manager      | Restricted         | Confidentiality          |
| Source code                              | GitHub                        | CTO             | Confidential       | Integrity                |
| The app itself (service uptime)          | AWS                           | CTO             | Internal           | Availability             |
| Backups                                  | AWS (separate backup storage) | IT Manager      | Restricted         | Availability             |

## 4. Cybersecurity Threats

MapleCloud faces several cybersecurity threats that could affect its
data, systems and customers. Many of these threats are made worse by
current weaknesses, such as missing MFA, untested backups and
unencrypted laptops. The main threats are listed below.

| **Threat**                          | **What could happen**                                                                                                                                                                                       | **Asset affected**                     |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| Phishing                            | An attacker tricks an employee into giving their Microsoft 365 password. Without MFA, the attacker can log in.                                                                                              | Employee HR and payroll records        |
| Ransomware                          | Attackers encrypt MapleCloud's systems. Backups have never been tested, so the company may not be able to restore its data and may be pushed to pay the ransom, with no guarantee of getting the data back. | Customer invoices, the app, backups    |
| Lost or stolen laptop               | Some laptops are not encrypted. If one is lost or stolen, anyone can read the files on it without needing to hack anything.                                                                                 | Customer data, HR records, source code |
| Insider threat (ex-employee access) | Former employees' accounts sometimes stay active. An ex-employee could log in and copy or change data after leaving.                                                                                        | Customer data, source code             |
| Weak policies and access control    | Only one policy exists, and staff can access more than their job needs (no least privilege). Mistakes or misuse are more likely and harder to detect.                                                       | All assets                             |

## 5. Governance Responsibilities

Security at MapleCloud is a shared responsibility. The table below shows
each role's main security duties.

| **Role**           | **Security responsibility**                                                                                                                |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| CEO                | Approves security policies and budget, and is ultimately accountable for security at MapleCloud                                            |
| CTO                | Keeps the source code secure and makes sure AWS is securely configured and available                                                       |
| IT Manager         | Manages user accounts and MFA, encrypts all laptops, removes access for leavers, and makes sure backups are tested regularly               |
| HR Manager         | Tells IT when people join, change roles or leave, so their access can be added, changed or removed on time                                 |
| Junior GRC Analyst | Writes and maintains security policies, keeps the risk register, checks that access rules are followed, and prepares the company for SOC 2 |
| All employees      | Follow security policies, complete security training, protect their passwords and devices, and report suspicious emails or activity to IT  |

## 6. Why GRC Is Important

MapleCloud needs a GRC program for several reasons. First, the company
is trying to sign its largest customer, a regional credit union, and the
deal depends on MapleCloud providing a SOC 2 report. Second, the company
faces serious risks such as ransomware and unauthorized access by former
employees, made worse by weaknesses like untested backups and a lack of
staff security training. Third, MapleCloud holds personal information,
so it must comply with PIPEDA, Canada's federal privacy law, and with
Quebec's Law 25 for its Quebec customers. In the future, customers may
also ask for ISO 27001 certification, and the company may face external
audits, so it needs to be prepared. Finally, a strong GRC program builds
customer trust, which MapleCloud needs as it grows.

## 7. GRC Objectives

Over the next 12 months, MapleCloud's GRC program will focus on the
following objectives:

| **\#** | **Objective**                                                                                    | **Target**                 | **Owner**                  |
|--------|--------------------------------------------------------------------------------------------------|----------------------------|----------------------------|
| 1      | Turn on MFA for all accounts                                                                     | Within 3 months            | IT Manager                 |
| 2      | Disable a leaver's accounts within 24 hours of their last day                                    | Within 3 months            | HR Manager and IT Manager  |
| 3      | Encrypt all company laptops                                                                      | Within 3 months            | IT Manager                 |
| 4      | Test backup restores every 3 months                                                              | First test within 2 months | IT Manager                 |
| 5      | Write and approve core security policies (access control, passwords, incident response, backups) | Within 4 months            | Junior GRC Analyst         |
| 6      | Train all employees in security awareness, then repeat yearly                                    | Within 6 months            | Junior GRC Analyst         |
| 7      | Complete a PIPEDA and Quebec Law 25 privacy review                                               | Within 6 months            | Junior GRC Analyst         |
| 8      | Be ready for a SOC 2 Type I audit                                                                | Within 9–12 months         | Junior GRC Analyst and CTO |

## 8. Laws and Regulations

MapleCloud must comply with Canadian privacy laws and is being asked by
customers to meet recognized security standards. These are summarized
below.

| **Law / Standard** | **Type**                                    | **Why it applies to MapleCloud**                                                     | **Key requirements**                                                                                             |
|--------------------|---------------------------------------------|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| PIPEDA             | Federal law (mandatory)                     | MapleCloud is a private business in New Brunswick that collects personal information | Consent, limited use, proper safeguards, report serious breaches to the Privacy Commissioner and affected people |
| Quebec Law 25      | Provincial law (mandatory)                  | MapleCloud has customers in Quebec                                                   | Named privacy officer, privacy impact assessments, report serious incidents to Quebec's regulator (CAI)          |
| SOC 2              | Audit standard (voluntary, customer-driven) | The credit union requires a SOC 2 report before signing                              | Controls based on the Trust Services Criteria, checked by an independent CPA audit (Type I, then Type II)        |
| ISO 27001          | International standard (voluntary)          | Larger customers may ask for it in the future                                        | A formal Information Security Management System (ISMS), risk assessment, and certification by an outside auditor |
| PCI DSS            | Industry standard                           | MapleCloud accepts card payments, but through Stripe                                 | Mostly handled by Stripe, since MapleCloud doesn't store card data                                               |

---

📄 Word version: [MapleCloud_GRC_Company_Profile.docx](MapleCloud_GRC_Company_Profile.docx)
