pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout the source code from your version control system (e.g., Git)
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], userRemoteConfigs: [[url: 'https://github.com/huynhtrunghieu9506/demo-jenkins.git']]])
            }
        }

        stage('Build') {
            steps {
                // Use a tool such as Maven or Gradle to build the Spring Boot project
                bat 'mvn clean package'
            }
        }

        stage('Test') {
            steps {
                // Run tests, if applicable
                bat 'mvn test'
            }
        }

    }
}
