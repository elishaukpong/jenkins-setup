pipeline {
  agent any
  stages {
    stage('Building') {
      steps {
        sh 'aws ecr get-login-password --region eu-central-1 | docker login --username AWS --password-stdin 835950464690.dkr.ecr.eu-central-1.amazonaws.com'

                  docker.image('835950464690.dkr.ecr.eu-central-1.amazonaws.com/php').pull()
                  docker.image('835950464690.dkr.ecr.eu-central-1.amazonaws.com/mysql').pull()

      }
    }
  }
}