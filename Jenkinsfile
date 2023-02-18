pipeline{
    agent any
    stages{
        stage('Checkout'){
            steps{
                git 'https://github.com/ashaavi/multibranch1.git'
                
            }
        }
        stage('Build Stage'){
            steps{
                sh 'mvn clean install'
            }
        }
        stage('Sonarqube Analysis'){
            steps{
                withSonarQubeEnv('sonarQube') {
                    sh 'mvn clean test sonar:sonar -Dsonar.projectkeys=sonarj'
    
                }
            }
        }
    }
}
    
