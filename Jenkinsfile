pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout([$class: 'GitSCM',
    branches: [[name: '*/main']],
    doGenerateSubmoduleConfigurations: false,
    extensions: [[$class: 'CloneOption', timeout: 60]], // timeout in minutes
    userRemoteConfigs: [[url: 'git@github.com:harmannoor2002/pra.git', credentialsId: 'd472490d-5c6f-47f2-a51d-e624103f0ebd']]
])

            }
        }

        stage('Build') {
            steps {
                echo "Building the project..."
            }
        }

        stage('Test') {
            steps {
                echo "Running tests..."
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploying..."
            }
        }
    }
}
