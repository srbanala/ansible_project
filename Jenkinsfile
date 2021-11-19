pipeline {
    agent any
        environment {
           DOCKER_CREDS=credentials('docker_id')
           }
    stages {
       stage(' build') {
          steps {
             sh 'chmod -R 777 * '
             sh ' /home/ec2-user/.local/bin/ansible all -m ansible.builtin.shell -a "echo welcome"   -u ec2-user --private-key /tmp/mykp.pem --become '
              }
      }
    }
    }
