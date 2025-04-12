pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh './gradlew build' // If using Gradle
                // sh 'mvn clean install' // Uncomment this if using Maven instead
            }
        }

        stage('Test') {
            steps {
                sh 'java -jar your-selenium-tests.jar'
            }
        }
    }
}
  post {
        always {
            archiveArtifacts artifacts: '**/build/libs/*.jar', fingerprint: true
            junit '**/build/test-results/test/*.xml'
        }
    }
}
