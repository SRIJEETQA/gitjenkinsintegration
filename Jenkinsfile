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
                // Use Maven instead of Gradle for the build process
                sh 'mvn clean install'
            }
        }
        stage('Test') {
            steps {
                // Assuming you're running Selenium tests here
                sh 'java -jar your-selenium-tests.jar'
            }
        }
    }
}
