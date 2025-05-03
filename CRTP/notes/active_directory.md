# Active Directory

**Active Directory (AD)** is a directory service developed by Microsoft that is used to manage and organize resources like users, computers, and groups in a networked environment. It provides a centralized way to control access, apply policies, and enable authentication across an organization’s IT infrastructure.

&nbsp;
## Active Directory Component and Structure

&nbsp;
## Component and Structure
| Windows Active Directory | Analogy |
| --- | --- |
| **Forest** | Nation |
| **Domain** | Province in Nation |
| **Domain Controller (DC)** | Governor’s office of province |
| **Organization Unit (OU)** | City in Province |
| **Groups** | District in City |
| **Trusts** | Alliance between Province |
| **Group Policies Object (GPO)** | Laws passed by Governor (DC) |
| **Schema** | Nation’s constitution |
| **Kerberos** | Nation’s passport and visa system |

&nbsp;
## Active Directory Core Concepts

### Forest
**Analogy:** The forest is like a **nation**. It contains multiple **provinces** (domains), and they all follow the same laws.
- A forest is a collection of **domains**. It’s the largest unit in Active Directory.
- All domains in a forest share the same **schema** (rules and data structure) and can communicate with each other.

&nbsp;
### Domain
**Analogy:** A domain is a **province** within the **nation** (forest). Each province has its own citizens (users/computers) and local rules but is still part of the nation.
- A domain is a logical group of users, computers, and resources managed under one administrative boundary.
- Each domain has its own **database** and serves as a **security boundary** for resource sharing and access control.

&nbsp;
### Domain Controller (DC)
**Analogy:** A domain controller is like the **governor’s office** of a province. It keeps **records** of everyone, **enforces laws** (policies), and **controls access** to resources.
- A DC is a server running Active Directory services.
- It is responsible for **authenticating users**, **applying policies**, and **managing** access to domain resources.
- If you control the DC, you control the domain.

&nbsp;
### Organizational Units (OUs)
**Analogy:** OUs are like **cities** within a **province**. Each city can have its own rules or policies (e.g., different curfews).
- OUs are containers used to organize users, computers, and other objects within a domain.
- They allow administrators to apply specific **Group Policies** to segments of the domain without affecting the entire domain.

&nbsp;
### Groups
**Analogy:** Groups are like **districts** within a city. They simplify management by grouping individuals with common roles or access needs.
- A group is a collection of users or computers that share the same permissions.
- Permissions and access control can be assigned to groups instead of managing users one by one.

&nbsp;
### Trusts
**Analogy:** Trusts are like **alliances** between provinces (domains or forests).
- Trusts define relationships between domains or forests that allow resource sharing and cross-domain authentication.
- Trusts can be **one-way** or **two-way**, determining access flow between trusted and trusting parties.

&nbsp;
### Group Policy Objects (GPOs)
**Analogy:** GPOs are like **laws passed by the governor**. These laws can apply to an entire province (domain) or just specific cities (OUs).
- GPOs are sets of rules and configurations applied to users and computers in a domain or OU.
- They enforce **security settings**, **application policies**, and **environment restrictions** across the organization.

&nbsp;
### Schema
**Analogy:** The schema is the **constitution** of the nation. It defines the roles and attributes of every type of citizen (object) in Active Directory.
- The schema is the master blueprint that defines **objects** (users, computers, groups) and their **attributes**.
- All domains in a forest share the same schema to maintain consistent structure and behavior.

&nbsp;
### Kerberos
**Analogy:** Kerberos works like a **passport and visa system**. Once logged in, you receive a **ticket** that proves your identity to other services.
- Kerberos is the default **authentication protocol** in Active Directory.
- It issues **tickets** that allow secure access to resources without repeatedly transmitting passwords.
