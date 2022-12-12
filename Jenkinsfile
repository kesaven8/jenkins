pipeline {
    agent any
    tools {
        maven 'maven-3.8.6'
        jdk 'jdk17'
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh 'printenv'
                sh 'mvn --version'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                sh 'mvn test'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying..'
                sh 'mvn deploy'
            }
        }
    }
}
