pipeline {
    agent any
    stages {
        stage ('Compile Stage') {

            steps {
                // sh mvn -B -DskipTests clean package
                echo 'this is simple build'

                
            }
        }
        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'apache-maven-3.6.3') {
                    bat 'mvn test'
                }
            }
        }
        stage ('Install Stage') {
            steps {
                withMaven(maven : 'apache-maven-3.6.3') {
                    bat 'mvn install'
                }
            }
        }
    }
}
