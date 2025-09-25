pipeline {
    agent any
    environment {
        JAVA_HOME = "C:\\Program Files\\Java\\jdk-21"
        MAVEN_HOME = "C:\\Program Files\\Apache\\Maven\\apache-maven-3.9.11"
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
        }.
    }
}
