pipeline {
    agent any

    tools {
        maven 'Maven'
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building using Maven...'
                bat 'mvn clean compile'
            }
        }

        stage('Run') {
            steps {
                echo 'Running project...'
                bat 'mvn exec:java'
            }
        }
    }
}