pipeline {
    agent any

    environment {
        DIRECTORY_PATH = '/var/jenkins_home/workspace/app'
        TESTING_ENVIRONMENT = 'Testing'
        PRODUCTION_ENVIRONMENT = 'Anshika'
    }

    stages {
        stage('Build') {
            steps {
                echo "Fetch the source code from the directory path specified by the environment variable: ${DIRECTORY_PATH}"
                echo "Compile the code and generate any necessary artefacts"
            }
        }

        stage('Test') {
            steps {
                echo "Unit tests"
                echo "Integration tests"
            }
        }

        stage('Code Quality Check') {
            steps {
                echo "Check the quality of the code"
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploy the application to a testing environment specified by the environment variable: ${TESTING_ENVIRONMENT}"
            }
        }

        stage('Approval') {
            steps {
                echo "Waiting for approval..."
                sleep time: 10, unit: 'SECONDS'
            }
        }

        stage('Deploy to Production') {
            steps {
                echo "Deploy the application to the production environment: ${PRODUCTION_ENVIRONMENT}"
            }
        }
    }
}
