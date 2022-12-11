env.JAVA_HOME="${tool 'jdk17'}"
pipeline {
    agent any
    tools {
        maven 'maven-3.8.6'
        jdk 'jdk17'
    }

    stages {
        stage('Build') {
            environment {
                JAVA_HOME="${tool 'jdk17'}"
            }
            steps {
                echo 'Building..'
                sh 'printenv'
                echo "JAVA_HOME"
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
