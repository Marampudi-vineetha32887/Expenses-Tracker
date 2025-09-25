pipeline {
    agent any

    tools {
        jdk "JDK"         // Make sure JDK is configured in Jenkins
        maven "Maven"     // Make sure Maven is configured in Jenkins
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/Marampudi-vineetha32887/Expenses-Tracker.git'
            }
        }

        stage('Build') {
            steps {
                bat 'mvn clean install'
            }
        }

        stage('Run App') {
            steps {
                bat 'mvn spring-boot:run'
            }
        }
    }

    post {
        success {
            echo 'Build and run successful!'
        }
        failure {
            echo 'Build failed!'
        }
    }
}
