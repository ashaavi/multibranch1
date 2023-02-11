pipeline {
         agent any
         stages {
                 stage('Build') {
                 steps {
                     echo 'this is build stage'
                 }
                 }
                 stage('Test') {
                 steps {
                    input('this is test stage')
                 }
                 }
                 stage('Deploy') {
                  
                       stage('Deploy start ') {
                           steps {
                                echo 'this is deploy stage'
                           } 
                           }
                 }
         }
