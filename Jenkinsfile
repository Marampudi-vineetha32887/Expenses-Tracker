pipeline {
    agent any
    environment {
        // Update these paths to match your system
        JAVA_HOME = "C:\\Program Files\\Java\\jdk-17" 
        MAVEN_HOME = "C:\\apache-maven-3.9.6"

        PATH = "${JAVA_HOME}\\bin;${MAVEN_HOME}\\bin;${env.PATH}"
    }
    stages {
        stage('Check Versions') {
            steps {
                bat 'java -version'
                bat 'mvn -version'
            }
        }
        stage('Build') {
            steps {
                bat 'mvn clean install'
            }
        }
    }
}

