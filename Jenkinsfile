pipeline {
    agent any
    tools {
        maven 'MAVEN_HOME'
    }
    stages{
        stage('Build'){
            steps{
                 sh script: 'mvn clean package'
                 }
         }
       
    }
            stage('Upload War To The Nexus'){
            steps{
            nexusArtifactUploader artifacts: [
            [
            artifactId: 'junit', 
            classifier: '', 
            file: 'target/simple-app-3.0.0-SNAPSHOT.war',      type: 'war'
           ]
          ], 
          credentialsId: 'nexus2', 
          groupId: 'in.javahome', 
          nexusUrl: '192.168.189.155:8081/', 
          nexusVersion: 'nexus2', 
          protocol: 'http', 
          repository: 'http://192.168.189.155:8081/repository/maven-test/', 
          version: '3.0.0-SNAPSHOT'
                 }
         }

}


