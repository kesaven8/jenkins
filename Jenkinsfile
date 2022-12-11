pipeline {
    agent {
        docker {
          image 'openjdk:17-jdk-alpine'
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
