pipeline {
    agent any
        environment {
           DOCKER_CREDS=credentials('docker_id')
           }
    stages {
       stage(' build') {
          steps {
             sh '/home/ec2-user/.local/bin/ansible-playbook site.yml --private-key /tmp/mykp.pem --limit dbservers --become  '
             }
       }
      }
    }
