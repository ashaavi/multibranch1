pipeline{
    agent any

stages{
    stage('Checkout'){
        steps{
            git 'https://github.com/ashaavi/java-example.git'
        }
    }
    stage('Build'){
       steps{
           sh 'mvn clean install'
       }
}
    stage('Test'){
        steps{
             withSonarQubeEnv('sonarque server'){
             sh 'mvn sonar:sonar'
             }
        }
    }

}
}
