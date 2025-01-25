pipeline {   
    agent { label 'slave' } 
  //  tools{
    //    jdk 'jdk17'
     //   maven 'maven3'
//	}
 
    	

    stages {
        stage('Git checkout') {
            steps {
                git branch: 'main', changelog: false, poll: false, url: 'https://github.com/hhgsharish/jenkins_project_1.git'
            }
        }
        
        stage('Compile') {
            steps {
                sh "mvn compile"
                 }
        }
        
        stage('Package') {
            steps {
                sh "mvn clean package"
                
                 }
        }
        
        
         
    }
}
