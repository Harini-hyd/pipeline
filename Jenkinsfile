pipeline{
    agent any
    tools{
        maven 'maven'
    }
    stages{
        stage('Checkout'){
            steps{
                git branch:'master',url:'https://github.com/Harini-hyd/pipeline.git'
            }
        }
        stage('Build'){
            steps{
                bat 'mvn clean package'
            }
        }
        stage('Test'){
            steps{
                bat 'mvn test'
            }
        }
        stage('Run Application'){
            steps{
                bat 'java -jar target/pipeline-0.0.1-SNAPSHOT.jar'
            }
        }
    }
}
