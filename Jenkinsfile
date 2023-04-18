pipeline {
    agent any

    stages {
        stage('git clone') {
            steps {
                git branch: 'main', url: 'https://github.com/arunpateldaynilgroup/Jenkins-pipeline.git'
            }
        }
        
        stage('clean and test') {
            steps {
                bat "mvn clean test"
            }
        }
                
        stage('build') {
            steps {
                bat "mvn package"
            }
        }        
    }
}
