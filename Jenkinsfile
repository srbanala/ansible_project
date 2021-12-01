pipeline {
    agent any
        environment {
           DOCKER_CREDS=credentials('docker_id')
           }
    stages {
       stage(' build') {
          steps {
             sh 'chmod -R 777 * '
             sh ' ansible-playbook site.yml -i hosts  -u ec2-user --private-key /tmp/mykp.pem -u ec2-user --become '
              }
      }
    }
    }
