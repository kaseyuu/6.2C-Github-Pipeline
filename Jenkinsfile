pipeline {
  agent any
  environment {
    DIRECTORY_PATH = 'C:\\Users\\YOU WU\\Desktop\\deakin\\753\\w6'
    TESTING_ENVIRONMENT = 'testing-environment'
    PRODUCTION_ENVIRONMENT = 'Kasey'
  }
  stages {
    stage('Build') {
      steps {
        echo "fetch the source code from $DIRECTORY_PATH"
        echo 'compile the code and generate any nfecessary artifacts'
        echo 'Use build automation tools like Maven or npm.'
      }
    }
    stage('Unit and Integration Tests') {
      steps {
        echo 'unit tests'
        echo 'integration tests'
        echo 'Use test automation tools like Appium or Katalon.'
      }
    }
    stage('Code Analysis') {
      steps {
        echo 'Integrate a code analysis tool like SonarQube.'
      }
    }
    stage('Security Scan') {
      steps {
        echo 'Integrate a security scanning tool like OWASP ZAP.'
      }
    }
    stage('Deploy to Staging') {
      steps {
        echo 'Deploy the application to a staging server like AWS EC2.'
        echo "Deploying the application to a testing environment: $TESTING_ENVIRONMENT"
      }
    }
    stage('Integration Tests on Staging') {
      steps {
        echo'Integration test'
      }
    }
    stage('Deploy to Production') {
      steps {
        echo 'Deploy the application to a production server like AWS EC2.'
        echo "Deploying the code to the production environment: $PRODUCTION_ENVIRONMENT"
      }
    }
    post {
        failure {
            mail to: 'kaseywu130@gmail.com',
            subject: 'Pipeline Failed',
            body: 'The pipeline has failed. Please check the logs.',
        }
        success {
            mail to: 'kaseywu130@gmail.com',
            subject: 'Pipeline Succeeded',
            body: 'The pipeline has succeeded.',
        }
    }
  }
}
