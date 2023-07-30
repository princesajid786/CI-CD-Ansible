pipeline {
    agent any 
    stages {
        stage('Preparing') {
            steps{
                sh 'echo Preparing'
            }
        }
        stage('Git Pulling') {
            steps{
                git branch: 'master', url: 'https://github.com/AmanPathak-DevOps/CICD-Ansible.git'
            }
        }
        stage('Playbook Initializing') {
            steps{
                sh 'echo Playbook Initializing'
            }
        }
        stage('Playbook Running') {
            steps{
                ansiblePlaybook credentialsId: 'ansible-connect', disableHostKeyChecking: true, inventory: '/etc/ansible/hosts', playbook: 'Nginx-Uninstallation.yml'
            }
        }
        stage('Playbook deployed') {
            steps{
                sh 'echo Deployment done!!!!'
            }
        }
    }
}