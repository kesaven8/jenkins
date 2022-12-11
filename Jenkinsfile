
pipeline {
    agent any
    tools {
        maven 'maven-3.8.6'
        jdk 'jdk17'
    }
    environment {
        env.JAVA_HOME = ${tool 'jdk17'}
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                echo "JAVA_HOME: ${tool 'jdk17'}"
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
