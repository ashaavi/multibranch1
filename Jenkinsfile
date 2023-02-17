pipeline{
    agent any

stages{
    stage('Checkout'){
        steps{
            git 'https://github.com/ashaavi/multibranch1.git'
        }
    }
    stage('SonarQubeTest'){
        steps{
             withSonarQubeEnv('installationName: sonarQube'){
             sh 'mvn clean test sonar:sonar -Dsonar.projectkey=sonar'
             }
        }
    }
        stage('Quality Gate'){
            steps{
                timeout(time: 1, Unit: 'HOURS'){
                    waitForQualityGate abortPipeline: true
                }
            }
        }
        stage('Build'){
            steps{
                sh 'mvn clean install'
            }
        }
    }

}


