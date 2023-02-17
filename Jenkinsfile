pipeline{
    agent any

stages{
    stage('Checkout'){
        steps{
            git 'https://github.com/ashaavi/multibranch1.git'
        }
    }
    stage('Build'){
       steps{
           sh 'mvn clean install'
       }
}
    stage('Test'){
        steps{
             withSonarQubeEnv('admin'){
             sh 'mvn sonar:sonar'
             }
        }
    }

}
}
