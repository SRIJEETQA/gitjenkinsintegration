pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/SRIJEETQA/gitjenkinsintegration.git', branch: 'main'
            }
        }

        stage('Build') {
            steps {
                sh './gradlew build' // or 'mvn clean install' depending on your setup
            }
        }

        stage('Test') {
            steps {
                sh 'java -jar your-selenium-tests.jar'
            }
        }
    }
}
