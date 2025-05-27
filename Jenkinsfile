pipeline { 
    agent any 
    tools { 
          jdk 'JAVA_Home'
          maven 'maven' //Ensure name matches with configured  
    } 
    stages {
         stage('Clone') {
             steps {
                 git credentialsId : 'github-token' , url : 'https://github.com/Harini-hyd/pipeline.git'
             }
         }
     stage('Build') {  
            steps { 
                bat 'mvn clean package'  
            } 
      } 
     stage('Test') {  
            steps { 
                bat 'mvn test'  
            } 
      } 
     stage('Run Application') {  
            steps { 
                bat 'java –jar target/pipeline-0.0.1-SNAPSHOT.jar'  
            } 
      }
    }
}
