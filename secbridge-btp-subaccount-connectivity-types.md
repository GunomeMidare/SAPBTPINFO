Connections from on premise ABAP system to SAP BTP subaccount (Cloud)

| Area                  | AUthentication Type        | Assessment.            | ESA Compliant        |
|:––---------------------|:–---------------------------|:---–--------------------|:----------------------|
| Cloud Foundry          | ROPC.                       |                         |.                      |
| BTP Auditlog            | oAuth Client Credentials.    | Ok.                      |No                       |
| BTP Auditlog.           | oAuth mtls authentication.   | ok.                      | yes.                    |


# Connections from On-Premise ABAP System to SAP BTP Subaccount (Cloud)

| Area                  | Authentication Type                                      | Assessment                                                                 | ESA Compliant |
|-----------------------|----------------------------------------------------------|----------------------------------------------------------------------------|---------------|
| Cloud Foundry         | OAuth 2.0 Resource Owner Password Credentials (ROPC) Grant | **Not recommended** – Deprecated in OAuth 2.1 and discouraged by OAuth security best practices (exposes credentials, lacks MFA support). Prefer modern alternatives. | No            |
| BTP Audit Log         | OAuth 2.0 Client Credentials Grant                       | Good for machine-to-machine (M2M) scenarios. Use with strong secret management and rotation. | No            |
| BTP Audit Log         | OAuth 2.0 Client Credentials Grant with mTLS Client Authentication | **Recommended** – Stronger security via mutual TLS (X.509 certificates). Preferred for production environments. | Yes           |