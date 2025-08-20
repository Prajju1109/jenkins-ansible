pipeline {
    agent any
    stages {
        stage('Clone Git Repository') {
            steps {
                git branch: 'main', credentialsId: '2', url: 'https://github.com/Prajju1109/jenkins-ansible.git'
            }
        }

        stage('Run Ansible Playbook') {
            steps {
                ansiblePlaybook credentialsId: '1', disableHostKeyChecking: true, installation: 'Ansible2', inventory: 'inventory.ini', playbook: 'install_apache.yml', vaultTmpPath: ''
            }
        }
    }
}

