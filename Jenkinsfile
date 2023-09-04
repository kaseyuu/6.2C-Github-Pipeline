pipeline{
    agent any
    environment {
        DIRECTORY_PATH = "C:\\Users\\YOU WU\\Desktop\\deakin\\753\\w5"
        TESTING_ENVIRONMENT = "testing-environment"
        PRODUCTION_ENVIRONMENT = "Kasey"
    }
    stages {
        stage ('Build'){
            steps{
                echo "fetch the source code from $DIRECTORY_PATH"
                echo "compile the code and generate any necessary artifacts"
            }
        }
        stage ('Unit and Integration Tests'){
            steps{
                echo "unit tests"
                echo "integration tests"
            }
        }
        stage ('Code Analysis'){
            steps{
                echo "check the quality of the code"
            }
        }
        stage ('Security Scan'){
            steps{
                echo "Deploying the application to a testing environment: $TESTING_ENVIRONMENT"
            }
        }
        stage ('Integration Tests on Staging'){
            steps{
                script {
                    echo "Waiting for manual approval..."
                    sleep(time: 10, unit: 'SECONDS')
                    echo "Manual approval received, proceeding..."
                }
            }
        }
        stage ('Deploy to Production'){
            steps{
                echo "Deploying the code to the production environment: $PRODUCTION_ENVIRONMENT"
            }
        }
    }
}