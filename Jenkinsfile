pipeline {
    agent any
        environment {
           DOCKER_CREDS=credentials('docker_id')
           }
    stages {
       stage(' build') {
          steps {
             sh 'ansible-playbook site.yml --private-key /tmp/mykp.pem --limit dbservers --become  '
             }
       }
      }
    }
