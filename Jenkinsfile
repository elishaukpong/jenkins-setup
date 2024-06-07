pipeline {
  agent any
  stages {
    stage('Building') {
      steps {
        echo 'Building'
      }
    }

    stage('Testing') {
      steps {
        echo 'Testing'
      }
    }

    stage('Deploying') {
      steps {
        echo 'Deploying'
      }
    }

    stage ('Deploy') {
        input {
            message "Enter parameters"
            parameters {
                choice(
                    name: 'Bigger',
                    choices: ['staging1', 'staging2'],
                    description: 'Pick a stage:'
                )
                string(name: 'BRANCH', defaultValue: 'master', description: 'What Branch')
            }
        }
        steps {
          echo "You picked: ${STAGING}"
          echo "You picked: ${BRANCH}"
          echo "PATH=$PATH"
        }
      }

  }
}