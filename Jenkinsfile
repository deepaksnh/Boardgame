pipeline {
    agent any
    
  tools {
    jdk 'java21'
    maven 'maven3.9'
}
    
    stages {   
        stage('Compile') {
            steps {
            sh 'mvn compile'
            }
        }
        stage('Package') {
    steps {
        sh 'mvn clean package -DskipTests'
    }
}
        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
        
        stage('Build') {
            steps {
                sh 'mvn package'
            }
        }
    }
}
