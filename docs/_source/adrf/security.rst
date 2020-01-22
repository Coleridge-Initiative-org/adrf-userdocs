Security Model and Compliance
=============================

The security model for ADRF is based on The :fivesafes:`Five Safes framework <>`, a widely-accepted approach for making effective use of sensitive data.

.. image:: ../images/5safes.png
  :width: 800
  :alt: The concept of the Five Safes Framework

Safe Projects
-------------
	Is this use of the data appropriate, lawful, ethical and sensible?

The design of the ADRF ensures that only approved projects which follow the relevant legal and ethical considerations are allowed. User interactions only occur through access-controlled project workspaces for which approval is given typically time-limited.

Safe People
-----------
	Can the researchers be trusted to use it in an appropriate manner?

Access is only allowed for individuals who have been approved by the data stewards. They
must have completed Security Awareness training and their use is subject to careful review,
management, and tracking.

Safe Data
---------
	Does the data itself contain sufficient information to allow confidentiality to be breached?

Extensive import review processes guide restricted data into a secure, cloud-based data research
facility, where only the datasets required for approved uses are allowed. In addition, personally
identifiable information (PII) is typically hashed using a hash-based Message Authentication
Code (HMAC) algorithm.

Safe Settings
-------------
	Does the access facility limit unauthorized use or mistakes?

All data access and use must comply with FedRAMP Moderate rating. FedRAMP (Federal Risk and Authorization Management Program) is a government-wide program that provides a standardized approach to security, facilitating a shift from insecure, tethered, tedious IT toward more secure, mobile, nimble, and rapid practices. FedRAMP requires monthly scans and reporting to demonstrate the continuous monitoring required for any software platform in the program to maintain its certification. Those scans ensure that ADRF adheres to all FedRAMP controls based on NIST 800–53 Revision 4 standards plus additional controls specific to cloud computing.

Safe Outputs
------------
	Are the statistical results non-disclosive?

The FedRAMP boundary ensures that data cannot be downloaded, since the environment is isolated from the internet. Any data exported from the environment must go through disclosure review to ensure that no confidential data gets exported. The ADRF follows disclosure reviews follow the protocol of the Census.
