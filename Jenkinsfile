pipeline {
    agent any
    stages {
        stage ('Build') {
            steps {
                script {
                    sh 'ls -lahR'
                    sh '"ansible-playbook ./playbooks/create-vm.yml"'
                }
            }
        }
        stage('Test') {
            steps {
                sh 'echo "Hello from TEST stage"'
                sh 'echo "trigger should work"'
            }
        }
    }
}
