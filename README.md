# IAM Security Portfolio

Welcome to my Identity and Access Management (IAM) portfolio.

This repository documents hands-on labs I completed using Okta to practice identity lifecycle management, authentication, application access, role-based access control, and security monitoring.

The environments, companies, applications, and employee identities used in these projects are fictional and were created for training purposes.

## About Me

I am a cybersecurity professional with enterprise experience investigating security alerts, reviewing identity and authentication activity, analyzing logs, documenting findings, and escalating suspicious behavior.

I am expanding my hands-on IAM experience through practical labs involving user administration, authentication policies, application access, RBAC, automated provisioning, deprovisioning, and identity lifecycle management.

- [LinkedIn](https://www.linkedin.com/in/nicole-r-824708202)
- [GitHub](https://github.com/nicolerenderos)

## Featured Projects

### Project 1: Okta Group-Based Application Access, MFA, and OIDC

Configured a fictional Okta environment for Silkstar Solutions to demonstrate user onboarding, group-based application access, authentication requirements, and application integration.

#### Work Completed

- Created and configured a fictional employee identity.
- Created departmental security groups.
- Assigned the employee to the appropriate group.
- Configured access to the Silkstar Finance Portal.
- Enrolled the employee in Okta Verify.
- Tested a multifactor authentication challenge.
- Created and tested an OpenID Connect integration.
- Reviewed Okta authentication and policy-evaluation logs.
- Documented and sanitized the implementation evidence.

#### Skills Demonstrated

- Okta administration
- Identity onboarding
- User and group management
- Group-based application access
- Multifactor authentication
- Single sign-on concepts
- OpenID Connect
- Authentication policies
- Security-log review
- Access troubleshooting

---

### Project 2: Automated Joiner–Mover–Leaver Lifecycle and RBAC in Okta

Built an automated identity lifecycle workflow using department-based Okta group rules.

A fictional employee was automatically assigned Human Resources access during onboarding. When the employee transferred to Finance, Okta automatically removed the Human Resources group, assigned the Finance group, and provisioned access to the Silkstar Finance Portal.

During offboarding, the employee's account was deactivated, active sessions were cleared, and application access was removed.

[View the complete Project 2 walkthrough](project-2-jml-rbac/README.md)

#### Work Completed

- Created Human Resources and Finance security groups.
- Created active group rules using the user's department attribute.
- Simulated an employee joining the Human Resources department.
- Verified automatic assignment to `SS-Dept-HR`.
- Simulated an internal transfer from Human Resources to Finance.
- Verified automatic removal of Human Resources access.
- Verified automatic assignment to `SS-Dept-Finance`.
- Provisioned the Silkstar Finance Portal through group membership.
- Simulated employee offboarding by deactivating the account.
- Verified session clearing and application-access removal.
- Reviewed the complete lifecycle in the Okta System Log.
- Created sanitized evidence for the implementation.

#### Skills Demonstrated

- Joiner–Mover–Leaver lifecycle
- Role-Based Access Control
- Attribute-driven group rules
- Automated provisioning
- Automated access modification
- Automated deprovisioning
- Least privilege
- Group-based application assignment
- Session revocation
- Audit logging
- Identity lifecycle validation

## IAM Skills Demonstrated

- Identity and Access Management
- Okta Workforce Identity
- User lifecycle administration
- Joiner–Mover–Leaver processes
- Role-Based Access Control
- User and group administration
- Attribute-based automation
- Application provisioning and deprovisioning
- Multifactor authentication
- Single sign-on concepts
- OpenID Connect
- Authentication policy configuration
- Least-privilege access
- Security-log analysis
- Access troubleshooting
- Technical documentation

## Tools and Technologies

- Okta
- Okta Verify
- OpenID Connect
- GitHub
- Markdown
- Microsoft Sentinel
- Torq
- ServiceNow
- Palo Alto Cortex XDR

## Portfolio Goals

This portfolio is being developed to demonstrate practical skills relevant to roles such as:

- IAM Analyst
- Identity and Access Management Analyst
- Identity Governance Analyst
- Access Management Analyst
- Identity Operations Analyst
- Security Administrator
- Cybersecurity Analyst

Additional Okta, Microsoft Entra ID, and identity-governance projects will be added as I continue developing my IAM experience.
