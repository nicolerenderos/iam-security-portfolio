# Okta Group-Based Application Access with MFA and OIDC/PKCE

**Status:** Completed  
**Platform:** Okta Integrator Free Plan  
**Organization:** Silkstar Solutions (fictional)

## Project Overview

This project demonstrates secure, group-based access to a fictional Finance application using Okta. I configured users, groups, multifactor authentication, application assignments, OpenID Connect, PKCE, and authorization-server policies.

## Business Scenario

Silkstar Solutions needed to provide Finance employees with secure access to an internal Finance Portal. Access needed to be assigned through department membership rather than individually, and users were required to complete multifactor authentication.

## Objectives

- Create and manage a test workforce identity.
- Organize users through department-based groups.
- Assign application access through group membership.
- Require Okta Verify MFA.
- Configure an OIDC single-page application.
- Use the Authorization Code flow with PKCE.
- Configure an authorization-server access policy.
- Validate successful authentication and authorization.
- Troubleshoot access failures using system logs.

## Environment

- Okta Integrator Free Plan
- Test organization: Silkstar Solutions
- Test user: Maya Chen
- Application: Silkstar Finance Portal
- Groups:
  - `SS-All-Employees`
  - `SS-Dept-Finance`

All identities and business information used in this project are fictional.

## Implementation

### 1. Identity and Group Configuration

I created a fictional employee identity for Maya Chen and configured employment attributes, including her organization, department, and job title.

I created company-wide and department-specific groups and added Maya to:

- `SS-All-Employees`
- `SS-Dept-Finance`

### 2. Multifactor Authentication

I enrolled the test identity in Okta Verify. This required an additional possession-based authentication factor during the application sign-in process.

### 3. OIDC Application Configuration

I created the Silkstar Finance Portal as an OpenID Connect single-page application.

The application used:

- Authorization Code grant
- Proof Key for Code Exchange (PKCE)
- Redirect URI validation
- OpenID and profile scopes
- No client secret in the browser-based application

### 4. Group-Based Application Assignment

I assigned the Finance Portal to the `SS-Dept-Finance` group. Maya inherited access through her Finance-group membership instead of receiving a direct individual assignment.

This approach supports scalable administration and least privilege.

### 5. Authorization Policy

I configured an access policy on the default custom authorization server for the Silkstar Finance Portal.

The policy rule:

- Permitted the Authorization Code grant
- Applied to users assigned to the application
- Permitted the required scopes
- Used standard access-token lifetime settings

### 6. Validation

I tested the complete authentication and authorization flow through an OIDC testing client.

The successful test produced:

- A valid authorization code
- A successful PKCE code exchange
- An access token
- An ID token
- A matching state value

## Troubleshooting

During initial testing, Maya successfully entered her credentials and completed the MFA challenge, but Okta denied application access.

I reviewed the Okta system events and confirmed:

- User authentication was successful.
- The sign-on policy issued an MFA challenge.
- The challenge was completed successfully.
- The application assignment was inherited through the Finance group.

This showed that authentication and group assignment were working correctly. I then determined that the default custom authorization server did not have an access policy.

I created an application-specific access policy and Authorization Code rule, repeated the test, and successfully completed the OIDC flow.

## Results

The completed configuration demonstrated that:

- Finance-application access can be managed through group membership.
- MFA protects the authentication process.
- Application assignment and authorization-server policies work together.
- Authorization Code with PKCE securely supports a browser-based application.
- Okta logs can distinguish authentication success from authorization failure.

## Security Concepts Demonstrated

- Identity lifecycle administration
- Authentication versus authorization
- Multifactor authentication
- Group-based access control
- Least privilege
- Single sign-on
- OAuth 2.0
- OpenID Connect
- Authorization Code flow
- PKCE
- Access-policy configuration
- Identity troubleshooting
- System-log analysis

## Evidence

Sanitized screenshots will demonstrate:

1. Department group configuration
2. Test-user group membership
3. Group-based application assignment
4. MFA enrollment
5. Authorization-server policy and rule
6. Successful OIDC authorization result

> Sensitive values—including tokens, authorization codes, client identifiers, tenant information, email addresses, and QR codes—are excluded or redacted.
