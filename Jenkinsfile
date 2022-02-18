pipeline {
    agent any
    stages {
        stage ('Build') {
            steps {
                script {
                    sh 'ls -lahR'
                    /* groovylint-disable-next-line GStringExpressionWithinString, LineLength */
                    sh 'ansible-playbook ./playbooks/create-vm.yml --extra-vars "vcenter_hostname=${vcenter_hostname} vcenter_username=${vcenter_username} vcenter_password=${vcenter_password} vm_uuid=${vm_uuid} " -e "ansible_python_interpreter=/usr/bin/python3"'
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
