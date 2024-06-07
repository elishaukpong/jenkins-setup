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
                    name: 'STAGING',
                    choices: ['staging1', 'staging2', 'staging3', 'staging4', 'staging5', 'staging6', 'staging7', 'staging8', 'staging9'],
                    description: 'Pick a stage:'
                )
                string(name: 'BRANCH', defaultValue: 'master', description: 'BE branch')
                string(name: 'FE_BRANCH', defaultValue: ' ', description: 'leave empty if not needed')
            }
        }
        steps {
          echo "You picked: ${STAGING}"
          echo "You picked: ${BRANCH}"
          echo "You picked: ${FE_BRANCH}"
          echo "PATH=$PATH"
        }
      }

  }
}