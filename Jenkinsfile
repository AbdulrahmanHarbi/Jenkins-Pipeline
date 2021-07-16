pipeline {
    agent any 
    stages {
        stage('Clone Repository & clean') { 
            steps {
                sh "git clone https://github.com/AbdulrahmanHarbi/Jenkins-Pipeline.git"
                sh "mvn clean -f jenkins-maven"
            }
        }
        stage('Test') { 
            steps {
                "mvn test -f jenkins-maven" 
            }
        }
        stage('Deploy') { 
            steps {
                sh "mvn package -f jenkins-maven" 
            }
        }
    }
}