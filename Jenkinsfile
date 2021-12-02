pipeline {
    agent any
        environment {
           DOCKER_CREDS=credentials('docker_id')
           }
    stages {
       stage(' build') {
          steps {
             sh 'chmod -R 777 * '
             sh ' ansible-playbook site.yml  -i demo_aws_ec2.yaml  -u ec2-user --private-key /tmp/mykp.pem --become '
              }
      }
    }
    }
