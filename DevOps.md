System Development life Cycle(SDLC):
Plan → Code → Share Repository → Continuous Integration → Build → Test → Configuration Management → Deploy → Monitor

Configuration Management(CM):
Is the task of tracking and controlling changes in the software, part of the larger cross-disciplinary field of

Continuous Integration(CI) vs Continuous Deployment(CD):
CI is filling code as quickly as possible to get feedback whether the build is successful or not. Each commit will trigger a build and the corresponding test.
CD is every build ran will generate some artifact to be deployed continuously

Software as a service (SaaS):
Software distribution model in which a third-party provider host app and makes them available to customer over the Internet.

Infrastructure as Code(IaC):
IaC is automation of IT operations (build, deploy, manage) by provisioning of code, rather than manual process. Provisioning of Dev, Test and Prod environment by writing code in one centralized location.

Docker Image:
Docker image is the source of Docker container. Docker images are used to create containers. Images are created with the build command, and produce a container when started with run.

Docker Container:
Docker containers include the application and all of its dependencies but share the kernel with other containers, running as isolated processes in user space on the host operating system. Docker containers are not tied to any specific infrastructure: they run on any computer, on any infrastructure and in any cloud.

Docker Hub:
Docker hub is a cloud-base registry service which allows you to link to code repositories, build your images and test them, stores manually pushed images and links to Docker clouf so you can deploy images to your hosts


What’s DevOps?
Practice brings developers, operations, HR, testing, their operations and their activities together in a collaborative fashion using proper processes and techniques to achieve the fastest and reliable software releases. The GOAL is producing faster releases with high quality.

Hows DevOps different from Agile?
Agile is a methodlogy and DevOps is a practice. Agile framework define a particular processes and rules and all the development has to fit into that framework. Framework or methodology only deals with development start and development end it doesn’t deal with how to test, how to release the code or how the operations and production support work ongoing. DevOps is the end-to-end SDLC starting from development, testing, operating, and production support, not just a framework, each organization can define its unique DevOps practice to meet their needs.

What is the need for DevOps?
Increase deployment frequency
 in order to sustain in the market, company need to do respond to changes as quickly as possible
New change = new deployment = new release
Lower failure rate of new releases
How fast to identify an issue
How fast you can fix that issue
Faster means recovery in time of a new release failure, benefit from continuous monitoring(monitoring the app after your release is complete to proactively checking if the app is providing the required result or not and identifying small issues and gap then fix them as early as possible, instead of waiting until the failure happen which might cause business damage)
Shortened lead time between fixes
Faster mean time to recovery in the event of new release failure

Name some top DevOps tools and how these tools work together?
Which are the top DevOps tools? Which tools have you worked on?
The most popular DevOps tools are mentioned below:

Git : Version Control System tool
Jenkins : Continuous Integration tool
Selenium : Continuous Testing tool
Puppet, Chef, Ansible : Configuration Management and Deployment tools
Nagios : Continuous Monitoring tool
Docker : Containerization tool
Source control tool(e.g. Git): distributed version control management tool
Building and compiling tool(e.g. Maven): provide out of box features for compiling Java code and store the artifact in a proper way
Integrate tool(e.g. Jenkins): continuous integration tool can be integrated with test tools, web interfaces testing, functional testing
Deploy tool(e.g. puppet, CHEF, Ansible): provisioning system to have an environment ready up and running and testing servers and then deploy the app. Use docker for the micro service app, providing consistent computing and warming through the SDLC

What functions does Git performs in DevOps?
Store the code in a repository and able to share with team members. Then integrate source code with continuous integration tools, everytime changing the source code, automatically triggered build and tests and then apply configuration changes and deploy it and be monitored. All can be further automated

Explain Git’s distributed architecture.
In Git, how do you revert a commit that has already been pushed and made public?
git revert <name_of_commit>

How to find a list of files that has changed in a particular commit?
git diff-tree -r {hash}	(r means recursively)
OR
git diff-tree -no-commit-id -name-only -r {hash}	(only shows the file name)

How to squash(combine) last N commits into a single commit?
git reset -soft HEAD~N &&
git commit

What is Continuous Integration?
Based on commit you are doing, every commit that you do to the repository has to be immediately integrate changes to other collaborators to the master branch, then the integration server(e.g. Jenkins, bamboo) will built, test and deploy it.

Mention some commonly used Jenkins Plugins.
Jenkins will not work without plugins.

Explain Jenkins distributed architecture and what is the need for this architecture?
Jenkins is a distributed architecture. There is a master server configured with all the jobs and the requirements, then you can choose particular job to run on different server. These can all be automated by installing Jenkins slave on each nodes and running it.
Jenkins Master distribute its workload to the Slaves. Jenkins Slaves are required to provide the desire environment and work on the basis of requests received from Jenkins Master.
The single Jenkins server was not enough to meet requirements like:
Sometimes need several different environments to test your builds, this cannot be done by a single Jenkins server
Larger and heavier project get built on a regular basis then a single Jenkins server cannot simply handle the entire load

How will you secure Jenkins?
Ensure global security is on
Endure Jenkins is integrated with company’s user directory with appropriate plugin
Ensure that matrix/project matrix is enabled to fine tune access
Automate the process of setting rights/privileges in Jenkins with custom version controlled script
Limit physical access to Jenkins data/folders
Periodically run security audits on same

Explain how to create a backup and copy files in Jenkins?
Move a job from one installation of Jenkins to another by simply copying the corresponding job directory
Make a copy of an existing job by making a clone of a job directory by a different name
Rename an existing job by renaming a directory

What are the goals of Configuration management processes?
The purpose of Configuration Management (CM) is to ensure the integrity of a product or system throughout its life-cycle by making the development or deployment process controllable and repeatable, therefore creating a higher quality product or system. The CM process allows orderly management of system information and system changes for purposes such as to:

Revise capability,
Improve performance,
Reliability or maintainability,
Extend life,
Reduce cost,
Reduce risk and
Liability, or correct defects.
