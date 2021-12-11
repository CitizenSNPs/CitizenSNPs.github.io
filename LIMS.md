Development and Process Design

In my time as an Automation Engineer, I took on managing the DevOps of a large Laboratory Information Management System (LIMS) application. The aim of the application was to handle data migration from the Illumina sequencers to and from the company's isilon spaces; this involved setting up the DevOps environment (Rancher 2.x), setting up virtual nodes, and migrating previous data to the new Rancher environment. This way, I could migrate old data and connect lab users to their respective projects by migrating old data to the new environment. One of the largest scoped projects of my career was to lead in the design, development, and procurement effort for a replacement LIMS via AWS Lambda and Illumina’s InterOp sequencing library, and single-handedly maintained frontend (AngularJS), DevOps (Rancher), and backend/database (MySQL) operations for Illumina’s CORE LIMS system, SAGE/Rex. This involved leading a large interdepartmental team of subject matter experts to choose a platform, create user & software requirements, and lead in a year and a half long software procurement initiative.

###Design & Development

First comes user requirements. In this case, the LIMS system encapsulates several stakeholders from several different LabOps groups, including Software Development, DevOps, and the CORE sequencing team. When dealing with a large collaborative group, it is vital to keep the different perspectives and expectations about the the future system in mind to ensure clarity and to capture and uncover user requirements in an efficient and effective manner. Once the user requirements are captured, I can build out software requirements that --- the capabilities and limitations of the LIMS platform. With this in mind, I was able to invent a new process that took the old system's AWS(S3) data pipeline and trasform it using AWS's Lambda service. The aim of this was to devliver secure data to and from the application at a reduced cost without exposing proprietary data from the company's isilon space, with the developed Lambda script acting as the pipeline's middleware.

Leaning on the requirements of the inplace LIMS application, I was able to create and develop a process that would take user requests and scrum any associated run data for relevant headers based on equipment type. I personally created the middleware script using Python 3 and Illumina's InterOp library, allowing me to read the sequencer's binary files from the asscociate isilon spaces and extract meaningful metrics to be delivered back to a Salesforce LIMS application as a single packaged JSON file.

https://illumina.github.io/interop/index.html

***include workflow diagram


