pipeline {
    agent any
    
            environment {
                        ANSIBLE_ROLE_NAME='splunk-uniforwarder'
                      }
    
    stages {
        stage('Build version') {
           steps {
                echo 'Hello Bitbucket'
                }
        }
        stage('Test Infra') {
            steps {
                echo 'Test is ok'
             }
          }
        stage('Ansible Role Deployment') {
            steps {
                sh 'ansible-playbook webhosting.yml'
             }
         }
        stage('Verify Deployment') {
            steps {
                sh 'ansible-playbook verify_webhosting.yml'
                  }
            }  
      }
      
    }
