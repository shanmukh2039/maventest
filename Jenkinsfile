pipeline {
    agent any
    tools {
        maven 'MAVEN_HOME'
    }
        stages {
        stage ('Compile Stage') {
                steps {
               withEnv("maven : 'MAVEN_HOME") {
                    sh 'mvn clean'
                }
            }
        }
        stage ('Testing Stage') {
              steps {
              withEnv("maven : 'MAVEN_HOME") {
                    sh 'mvn test'
                }
            }
        }
    }
}


