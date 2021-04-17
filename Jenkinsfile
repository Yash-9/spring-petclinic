pipeline {
        agent {
            label 'master'
        }
        tools {
            maven 'mymaven'
            jdk 'myjava'
        }
    stages {
        stage ('Checkout the code') {
            steps{
                git branch: 'main', url: 'https://github.com/Yash-9/spring-petclinic.git'
            }
        }
        stage ('Code Compile') {
            steps{
                sh """
                mvn compile
                """
            }
        }
        stage ('JUNIT Test') {
            steps{
                sh """
                mvn test
                """
            }
        }
        stage ('Packaging') {
            steps {
                sh """
                mvn package
                """
            }
        }
      }   
}
