pipeline {
    agent any

    stages {

        stage('Clone GitHub Repository') {
            steps {
                git url: 'https://github.com/VeereshVBanakar/jenkins/new/main.git',
                branch: 'main'
            }
        }

        stage('Execute Ansible Playbook') {
            steps {
                sh '''
                sudo -u ansible ansible-playbook -i inventory install_nginx.yml
                '''
            }
        }

    }
}
