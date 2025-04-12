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
        sh 'mvn clean install'
    }
}

        }

        stage('Test') {
            steps {
                sh 'java -jar your-selenium-tests.jar'
            }
        }
    }
}
