pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
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
    post {
      failure {
        mail to: 'kaseywu130@gmail.com',
        subject: 'Test Failed',
        body: 'Test stage has failed.'
        }
      success {
        mail to: 'kaseywu130@gmail.com',
        subject: 'Test Succeeded',
        body: 'Test stage has succeeded.'
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
    post {
      failure {
        mail to: 'kaseywu130@gmail.com',
        subject: 'Security Scan Failed',
        body: 'Security Scan stage has failed.'
        }
      success {
        mail to: 'kaseywu130@gmail.com',
        subject: 'Security Scan Succeeded',
        body: 'Security Scan stage has succeeded.'
      }
    }
    stage('Deploy to Staging') {
      steps {
        echo 'Deploy the application to a staging server like AWS EC2.'
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
      }
    }
  }
}
