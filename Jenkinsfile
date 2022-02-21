pipeline {
    agent any
    stages {
        stage ('Build') {
            environment {
                vcenter_hostname = credentials('vcenter_hostname')
            }
            steps {
                script {
                    sh("echo ####vcenter_hostname####")
                    sh("echo vcenter_hostname is : ${vcenter_hostname}")
                    // sh 'ls -lahR'
                    // sh 'echo "vcenter_hostname is $vcenter_hostname"'
                    // sh 'echo "vcenter_hostname is ${str3}"'
                    /* groovylint-disable-next-line GStringExpressionWithinString, LineLength */
                // sh 'ansible-playbook ./playbooks/create-vm.yml --extra-vars "vcenter_hostname=${vcenter_hostname} vcenter_username=${vcenter_username} vcenter_password=${vcenter_password} vm_uuid=${vm_uuid}" -e "ansible_python_interpreter=/usr/bin/python3"'
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
