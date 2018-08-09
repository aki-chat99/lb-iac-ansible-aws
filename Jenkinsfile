pipeline {
  agent any
  stages {
    stage('Initialize') {
      parallel {
        stage('Initialize') {
          steps {
            echo 'creating infra using terraform'
          }
        }
        stage('Infra Build') {
          steps {
            ws(dir: '/var/lib/jenkins/demo1') {
              sh '''cd /var/lib/jenkins/demo1
pwd
#./iac_lb_ans_aws.sh'''
            }

          }
        }
      }
    }
  }
}