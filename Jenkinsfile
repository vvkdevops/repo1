pipeline {
    agent any
    environment{
        PATH = "/c/Program Files/apache-maven-3.6.3/bin:$PATH"

    stages {
        stage ('Compile Stage') {

            steps {
                withMaven(maven : 'maven_3_5_0') {
                    sh 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'maven_3_5_0') {
                    sh 'mvn clean test'
                }
            }
        }
    }
  }
}
