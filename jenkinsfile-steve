pipeline {
    agent any

    stages {

        stage('clean') {
            agent {
                 docker { image 'maven:3.8.5-openjdk-8-slim' }
             }

            steps {
               sh '''
              mvn clean
               '''
            }
        }

        stage('compile') {
            agent {
                 docker { image 'maven:3.8.5-openjdk-8-slim' }
             }

            steps {
               sh '''
             mvn compile
               '''
            }
        }

stage('validate') {
    agent {
                 docker { image 'maven:3.8.5-openjdk-8-slim' }
             }

            steps {
               sh '''
               mvn validate
               '''
            }
        }



stage('test') {
    agent {
                 docker { image 'maven:3.8.5-openjdk-8-slim' }
             }

            steps {
               sh '''
             mvn test 
               '''
            }
        }

stage('package') {
    agent {
                 docker { image 'maven:3.8.5-openjdk-8-slim' }
             }

            steps {
               sh '''
              mvn package
               '''
            }
        }

stage('verify') {
    agent {
                 docker { image 'maven:3.8.5-openjdk-8-slim' }
             }

            steps {
               sh '''
              mvn verify
               '''
            }
        }


stage('install') {
    agent {
                 docker { image 'maven:3.8.5-openjdk-8-slim' }
             }

            steps {
               sh '''
           mvn install
               '''
            }
        }
       


    }
}
