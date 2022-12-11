pipeline {
    agent {
        docker {
          image 'maven:eclipse-temurin-17-alpine'
            args '-u root:root'
        }
    }
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh 'mvn clean package'
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
