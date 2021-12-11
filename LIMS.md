Development and Process Design

At the beginning of 2020, I took on a large project to develop and maintain the backend environment for a large Laboratory Information Management System (LIMS) application. The aim of the application was to handle data migration from the Illumina sequencers to and from the company's isilon spaces. For a year and a half, I single-handedly maintained frontend (AngularJS), DevOps (Rancher), and backend/database (MySQL) operations for Illumina’s CORE LIMS system, SAGE/Rex, and migrated the application to a Rancher 2.x environment. This involved setting up the new Rancher environment and fitting it to a docker image, setting up the virtual nodes, and maintaining all user data from the existing system. This way, I could migrate old data and connect all lab users to their respective CORE projects by migrating old data to the new environment. 

One of the largest scoped projects of my career was to also lead the design, development, and procurement effort for a replacement LIMS system and to aid in its release by Spring 2021. This involved leading a large interdepartmental team of subject matter experts to choose a platform, create user & software requirements, and to help lead in a year and a half long software procurement initiative.

###Design & Development

I follow a personal workflow when introducing new systems to an existing pipline. 

**First comes user requirements.** What does the client need? In this case, the LIMS system encapsulates several stakeholders from several different LabOps groups, including Software Development, DevOps, and the CORE sequencing team. When dealing with a large collaborative group, it is vital to keep the different perspectives and expectations about the the future system in mind to ensure clarity and to capture/uncover user requirements in an efficient and effective manner. 

**Next come sofware requirements.** Once user reqs are captured, I can build out software requirements that highlights the capabilities and takes into the consideration the limitations of the software platform. With this in mind, I was able to invent a new process that took the laboratory's old AWS(S3) pipeline and trasform it using AWS's Lambda service. The aim of this was to deliver secure data to and from the application at a reduced cost without exposing proprietary data from the company's isilon space, with a developed Lambda script acting as the pipeline's middleware.

Leaning on the requirements of the inplace LIMS application, I was able to create and develop a process that would take user requests and scrum any associated run data for relevant headers based on equipment type. I personally created the middleware script using Python 3 and Illumina's InterOp library, allowing me to read the sequencer's binary files from the asscociate isilon spaces and extract meaningful metrics to be delivered back to a Salesforce LIMS application as a single packaged JSON file.

https://illumina.github.io/interop/index.html

***include workflow diagram


