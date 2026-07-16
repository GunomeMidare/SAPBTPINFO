
# Connections from On-Premise ABAP System to SAP BTP Subaccount (Cloud)

| Area                  | Authentication Type                                      | Assessment                                                                 | ESA Compliant |
|-----------------------|----------------------------------------------------------|----------------------------------------------------------------------------|---------------|
| Cloud Foundry         | OAuth 2.0 Resource Owner Password Credentials (ROPC) Grant | **Not recommended** – Deprecated in OAuth 2.1 and discouraged by OAuth security best practices (exposes credentials, lacks MFA support). Prefer modern alternatives. | No            |
| BTP CLI.              | OAuth 2.0 Resource Owner Password Credentials (ROPC) Grant | | |
| BTP Audit Log         | OAuth 2.0 Client Credentials Grant                       | Good for machine-to-machine (M2M) scenarios. Use with strong secret management and rotation. | No            |
| BTP Audit Log         | OAuth 2.0 Client Credentials Grant with mTLS Client Authentication | **Recommended** – Stronger security via mutual TLS (X.509 certificates). Preferred for production environments. | Yes           |
| Destination Service.  | OAuth 2.0 Client Credentials Grant.                      |      |.       |

SAP recommends that you use mTLS which uses an X.509 client certificate because it is a more secure way of authenticating.

- [Calling the Destination Service REST API](https://help.sap.com/docs/connectivity/sap-btp-connectivity-cf/calling-destination-service-rest-api?locale=en-US#2.-get-credentials)