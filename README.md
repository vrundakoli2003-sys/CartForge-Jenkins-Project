# CartForge Jenkins CI/CD Project

## Project Overview

CartForge is a Node.js application used to demonstrate
Continuous Integration and Continuous Delivery using Jenkins,
GitHub, and an Ubuntu-based AWS EC2 server.

The project demonstrates how source code can be managed in
GitHub and automatically built and packaged through a Jenkins
pipeline.

## Technologies Used

- Git
- GitHub
- Jenkins
- Node.js
- npm
- Linux / Ubuntu
- AWS EC2
- Bash Scripting

## Jenkins Pipeline

The Jenkins pipeline performs the following activities:

1. Retrieves the application source code from GitHub.
2. Installs the required Node.js dependencies.
3. Runs the application build process.
4. Creates the CartForge application artifact.
5. Archives the generated artifact.
6. Reports the pipeline result.

## Repository Structure

CartForge-Jenkins-Project/

├── README.md
├── Jenkinsfile
├── pipeline-report.txt
├── scripts/
│   ├── install-jenkins.sh
│   └── backup.sh
├── screenshots/
└── documentation/

## Backup

The `scripts/backup.sh` script creates a compressed backup
of the Jenkins data directory:

`/var/lib/jenkins`

The backup is stored in:

`/var/backups/jenkins/`

## Pipeline Monitoring

The pipeline execution details are documented in
`pipeline-report.txt`.

The report contains build number, execution time, trigger,
agent, result, failed stages, and generated artifact details.

## Project Status

The Jenkins pipeline has been successfully configured and
tested. Build #2 completed successfully with no failed stages
and generated the CartForge application artifact.
