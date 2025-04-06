pipeline {
    agent any
    tools {
        ansible 'ansible_default'
    }
    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/adnanhassanriar/colours.git', branch: 'main'
            }
        }
        stage('Run Ansible Playbook') {
            steps {
                ansiblePlaybook(
                    playbook: 'playbook.yml',
                    inventory: 'hosts',
                    become: true
                )
            }
        }
    }
}
