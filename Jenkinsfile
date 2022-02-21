pipeline {
    agent any
    stages {
        stage ('Build') {
            environment {
                SECRET_FILE_ID = credentials('vmwareSecrets')
            }
            steps {
                script {
                    echo "####DISPLAYING SECRET_FILE_ID####"
	                echo "Global property file: ${SECRET_FILE_ID}"
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
