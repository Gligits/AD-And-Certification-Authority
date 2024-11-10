# AD-Setting-Up-a-Secondary-Enterprise-Certification-Authority
Installing a root and a secondary CA, configure the CRL and AIA distribution points, and then verify that the entire system works as expected
# Architecture 
![Frame 136](https://github.com/user-attachments/assets/b9304f40-09f1-4e56-9fe0-7400c4dda8b0)

# First we are gonna install a Secondary Enterprise CA Using a Standalone Root CA:
- The root CA **installed in DC1** is the main authority responsible for issuing and signing digital certificates within an organization. It's usually set up as a standalone system to enhance security, as it should be as isolated as possible.

- The secondary (or subordinate) enterprise CA **installed in server1** will rely on the root CA for its trust hierarchy. The subordinate CA can issue certificates to end users and devices within the enterprise, but it's tied to the root CA for trust.

-> By separating the CAs, you increase security and flexibility. The root CA, being standalone and often offline, is less vulnerable to compromise, while the enterprise CA can handle day-to-day certificate management within the organization.

# Then we are gonna configure, implement and test Certificate Revocation List (CRL) and Authority Information Access (AIA) Points

- The Certificate Revocation List (CRL) is essential for managing and updating the status of certificates. If a certificate is compromised, expired, or no longer needed, it’s added to the CRL to alert systems not to trust it.

- Authority Information Access (AIA) points are configured so that users and systems can locate the CA’s certificates and verify their authenticity. This setup is particularly important for ensuring that all users and devices have reliable access to up-to-date certificate information.
