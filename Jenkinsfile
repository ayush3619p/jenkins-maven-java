pipeline {
    agent any

    tools {
        maven 'Maven'
    }

    stages {
        stage('Checkout Code') {
            steps {
                echo 'Pulling code from GitHub...'
                git 'https://github.com/ayush3619p/jenkins-maven-java.git'
            }
        }

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