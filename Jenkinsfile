pipeline {
    agent any
    def mvnHome 
    mvnHome = tool 'MAVEN_HOME'
        stages {
        stage ('Compile Stage') {
                steps {
               withEnv(["MAVEN_HOME=$mvnHome"]) {
                    sh 'mvn clean'
                }
            }
        }
        stage ('Testing Stage') {
              steps {
              withEnv(["MAVEN_HOME=$mvnHome"]) {
                    sh 'mvn test'
                }
            }
        }
    }
}


