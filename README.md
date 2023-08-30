# ansible-jenkins-pipeline

Deployment of Ansible Playbook using Jenkins Pipeline


## Description

**Automated Deployment with Ansible Playbook via Jenkins Pipeline**

* This repository demonstrates a streamlined process for deploying applications using Ansible playbooks through a Jenkins pipeline. 
* The integration of Ansible and Jenkins facilitates automated, consistent, and reproducible deployments, reducing manual intervention and ensuring efficient software delivery. 
* Follow the setup instructions to enable seamless deployment to target servers, all while benefiting from Jenkins' powerful automation capabilities. 
* Keep your deployments reliable and hassle-free by integrating Ansible and Jenkins today.

## Prerequisites
Before setting up the Jenkins pipeline for deploying Ansible playbooks, make sure you have the following:

- [x] **Jenkins Server**: Ensure you have a Jenkins server up and running.
- [x] **Ansible**: Ansible should be installed on the machine where the Jenkins server is running or on a dedicated deployment server.
- [x] **Target Servers**: Make sure you have the target servers or nodes where you want to deploy your playbook. Ansible should be able to access these servers.


## Setup Instructions

Follow these steps to set up the deployment process:

1. - Clone this Repository

2. - Configure Ansible: Modify the ansible.cfg and inventory.ini files in the repository according to your Ansible setup. Make sure you have defined the target servers properly.

3. - Create Jenkins Pipeline:
- Log in to your Jenkins server and create a new pipeline project.
- In the pipeline configuration, link your GitHub repository and specify the Jenkinsfile path as Jenkinsfile.

4. Update Jenkinsfile: Open the Jenkinsfile in this repository and make the following modifications:
- Adjust the ansiblePlaybook stage to point to your Ansible playbook file.
- Configure the necessary environment variables like ANSIBLE_CONFIG, ANSIBLE_HOST_KEY_CHECKING, etc., based on your needs.

5. - Credentials: Add any required credentials (SSH keys, Ansible vault password, etc.) to the Jenkins credentials store.

6. - Run Pipeline: Trigger the pipeline manually or set up webhooks to automatically trigger the pipeline whenever changes are pushed to the repository.


## Jenkins Pipeline Stages

- **Checkout:** This stage checks out the repository code from GitHub.

- **Check YAML Syntax:** Validates the syntax of your YAML files to prevent issues during playbook execution.

- **Check Markdown Syntax:** Ensures that your README and other markdown files have proper syntax and formatting.

- **Prepare Ansible Environment:** Sets up the environment for Ansible execution, ensuring required dependencies are installed.

- **Verify Ansible Playbook Syntax:** Checks the syntax of your Ansible playbook to catch errors before deployment.

- **Deploy App in Production:** Executes the Ansible playbook to deploy the application to the production servers.

- **Cleanup:** Performs any necessary cleanup tasks after the deployment.

&#x1F4DD; **Note:**
- Ensure that your Jenkins server has the required permissions to access the target servers using SSH or other authentication methods.

- It's recommended to run the Jenkins agent with limited privileges and provide only the necessary permissions for the deployment tasks.

- Regularly update the repository and Jenkins pipeline to incorporate any changes in your Ansible playbook or deployment process.


## Author

- [Mansour KA](http:mansourka.com)