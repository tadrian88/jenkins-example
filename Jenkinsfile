pipeline {
    agent any
    stages {
        stage ('Build') {
            steps {
                script {
                    withCredentials([file(credentialsId: 'vmware_secrets', variable: 'vmwaresecrets')]) {
                        sh 'ansible-playbook ./playbooks/create-vm.yml --extra-vars "@$vmwaresecrets" -e "ansible_python_interpreter=/usr/bin/python3"'
                    }
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
