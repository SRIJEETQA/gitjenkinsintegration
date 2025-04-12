pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/your-username/your-repo.git', branch: 'main'
            }
        }
        stage('Build') {
            steps {
                sh './gradlew build' // or `mvn clean install` depending on your project
            }
        }
        stage('Test') {
            steps {
                sh 'java -jar your-selenium-tests.jar'
            }
        }
    }
}
