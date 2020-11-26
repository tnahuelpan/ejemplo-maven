pipeline {
    agent any
    stages {
        stage('Compile'){
            steps{
                dir("D:\\\\Estudios\\\\ejemplo-maven"){
                    sh 'mvn clean compile -e'
                }
            }
        }
        stage('Test'){
            steps{
                dir("D:\\\\Estudios\\\\ejemplo-maven"){
                    sh 'mvn clean test -e'
                }
            }
        }
        stage('Jar'){
            steps{
                dir("D:\\\\Estudios\\\\ejemplo-maven"){
                    sh 'mvn clean package -e'
                }
            }
        }
        stage('Run'){
            steps{
                dir("D:\\\\Estudios\\\\ejemplo-maven"){
                    sh 'mvn spring-boot:run &'
                }
            }
        }
        stage('Sleep'){
            steps{
                dir(""){
                    sh 'sleep 10'
                }
            }
        }
        stage('Testing'){
            steps{
                dir("D:\\\\Estudios\\\\ejemplo-maven"){
                    sh 'curl -X GET "http://localhost:8081/rest/mscovid/test?msg=testing"'
                }
            }
        }
    }
}
