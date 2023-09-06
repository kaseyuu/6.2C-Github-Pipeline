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
      post {
        failure {
          emailext attachmentsPattern: '**/*.log',
          body: 'Test stage has failed.',
          subject: 'Test Failed',
          to: 'kaseywu130@gmail.com'
        }
        success {
          emailext attachmentsPattern: '**/*.log',
          to: 'kaseywu130@gmail.com',
          subject: 'Test Succeeded',
          body: 'Test stage has succeeded.'
        // subject: 'Test Succeeded',
        // body: 'Test stage has succeeded.',
        // to: 'kaseywu130@gmail.com'
        }
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
      post {
        failure {
          emailext attachmentsPattern: '**/*.log',
          body: 'Security Scan stage has failed.',
          subject: 'Security Scan Failed',
          to: 'kaseywu130@gmail.com'
        }
        success {
          emailext attachmentsPattern: '**/*.log',
          subject: 'Security Scan Succeeded',
          body: 'Security Scan stage has succeeded.',
          to: 'kaseywu130@gmail.com'
        }
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
  }
}
