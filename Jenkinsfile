pipeline {
    agent {
        label 'terraform-agent'
    }

    stages {

        stage('Oracle Health Check') {
            steps {
                sh '''
                ansible-playbook \
                -i ansible/inventory/inventory.ini \
                -u oracle \
                ansible/playbooks/check-pmon.yml
                '''
            }
        }
    }
}
