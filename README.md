# AD-Setting-Up-a-Secondary-Enterprise-Certification-Authority
Installing a root and a secondary CA, configure the CRL and AIA distribution points, and then verify that the entire system works as expected

![Frame 136](https://github.com/user-attachments/assets/b9304f40-09f1-4e56-9fe0-7400c4dda8b0)

- The root CA **installed in DC1** is the main authority responsible for issuing and signing digital certificates within an organization. It's usually set up as a standalone system to enhance security, as it should be as isolated as possible.

- The secondary (or subordinate) enterprise CA **installed in server1 **will rely on the root CA for its trust hierarchy. The subordinate CA can issue certificates to end users and devices within the enterprise, but it's tied to the root CA for trust.

-> By separating the CAs, you increase security and flexibility. The root CA, being standalone and often offline, is less vulnerable to compromise, while the enterprise CA can handle day-to-day certificate management within the organization.
