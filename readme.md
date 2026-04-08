# Microsoft Entra ID IAM Lab

The lab demonstrates
*  Role-based access control (RBAC)
*  Single Sign-On (SSO) configuration
*  Multi-Factor Authentication (MFA)
*  Identity Governance (Access Reviews, Entitlements)
*  Authentication troubleshooting using audit logs

# Objectives 
*  Implement group-based access control
*  Configure secure authentication flows
*  Simulate real IAM support scenarios
*  Build job-ready IAM experience

# User setup
![Alt Text](screenshots/users.png)
My account is the Global Admin and the rest are simulated employees

# Group Design
![Alt Text](screenshots/groups.png)
Model: User -> Group -> Resource

# Access Management
**Enterprise Application (SSO)**
*  Configured test application (SAML-based)
*  Group-based assignement
*  Engineering group -> App access

**Key Concept**
*  Eliminates direct user-to-app assignments
*  Improves scalability and auditability


![Alt Text](screenshots/sso2.png)
Signed into 'My Apps' panel under user account
![Alt Text](screenshots/sso3.png)
Given unique token for user account SSO
![Alt Text](screenshots/sso4.png)
Granted access to tool-kit

# 🛡️ Conditional Access Policies

**Policy 1: Require MFA**
*  Scope: All users
*  Grant Control: Require multi-factor authentication

**Policy 2: Admin Protection**
*  Scope: Admin roles
*  Controls:
*  Require MFA
*  Block legacy authentication

**Policy 3: Risk-Based Access**
*  Condition: High sign-in risk
*  Action: Block access

# 🔑 Authentication (MFA)
*  Microsoft Authenticator
*  MFA prompts
*  Login success/failure flows

# 🧾 Identity Governance

**Access Reviews**
*  Scope: SG-Engineering
*  Reviewer: Admin
*  Action: Approved/denied access

**Entitlement Management**
*  Created Access Package: “New Hire Bundle”
*  Includes: Group membership
*  Application access



# 📊 Monitoring & Logging

**Sign-in Logs used to analyze:**
*  Failed login attempts
*  MFA challenges
*  Conditional Access enforcement



**Audit Logs Tracked:**
	•	User changes
	•	Group assignments
	•	Policy updates



# 🧪 Troubleshooting Scenarios

**Scenario 1: User cannot access application**

Steps:
*  Verify group membership
*  Confirm app assignment
*  Check Conditional Access policies



**Scenario 2: MFA not prompting**

Steps:
*  Review Conditional Access scope
*  Confirm policy targeting
*  Validate authentication methods



**Scenario 3: Account blocked**

Steps:
*  Check sign-in logs
*  Identify risk conditions
*  Review applied policies



# 🧠 Key Takeaways
*  Group-based access is critical for scalable IAM
*  Conditional Access is the primary enforcement layer
*  Logs are essential for troubleshooting authentication issues
*  Identity Governance enables lifecycle management



# 🚀 Skills Demonstrated
*  Microsoft Entra ID administration
*  IAM policy design
*  SSO configuration (SAML)
*  Conditional Access implementation
*  MFA deployment
*  Identity Governance workflows
*  Authentication troubleshooting



# 🔧 Future Enhancements
*  Hybrid identity integration (on-prem AD + sync)
*  Privileged Identity Management (PIM)
*  Automated provisioning (SCIM)
*  Integration with additional SaaS applications

