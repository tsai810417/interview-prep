System Development life Cycle(SDLC):
Plan → Code → Share Repository → Continuous Integration → Build → Test → Configuration Management → Deploy → Monitor

Configuration Management(CM):
Is the task of tracking and controlling changes in the software, part of the larger cross-disciplinary field of

Continuous Integration(CI) vs Continuous Deployment(CD):
CI is filling code as quickly as possible to get feedback whether the build is successful or not. Each commit will trigger a build and the corresponding test.
CD is every build ran will generate some artifact to be deployed continuously

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
