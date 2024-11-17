# Creating a Custom Certificate Template
We are going to create a custom certificate template named "worker" for managing digital certificates in a Windows environment. 
Starting with connecting to a Certification Authority server (DC1) from the secondary server Server1.
we access the certificate management interface and duplicated the User certificate template. 
We customize it by naming it "Worker" , setting a validity period of six months and a renewal period of three months, specifying a minimum key size of 2048 bits, and requiring user input during enrollment. 
We disabled options to include email account details in the subject name, tailoring the template to meet specific organizational needs.

# Configuring Permissions for "worker" Certificate Enrollment
We configure the permissions to allow domain users to enroll for the Worker certificates. 
Using the Public Key Management tool, we accessed the properties of the worker  certificate template and modified its security settings. 
We grante the domain users "Read" and "Autoenroll" permissions by selecting the corresponding checkboxes under the "Allow" column. 
This ensures that users in the specified group can automatically enroll for certificates based on this template.
we closed all programs to complete the task.
