pipeline {
    agent any 
    tools {
         maven 'maven'
         jdk 'java'
    }
    stages {
        stage('Stage-1 : Clean') { 
            steps {
                sh 'mvn clean'
            }
        }
         stage('Stage-2 : Validate') { 
            steps {
                sh 'mvn validate'
            }
        }
         stage('Stage-3 : Compile') { 
            steps {
                sh 'mvn compile'
            }
        }
         stage('Stage-4 : Test') { 
            steps {
                sh 'mvn test -DskipTests'
            }
        }
          stage('Stage-5 : pacege') { 
            steps {
                sh 'mvn pacege -DskipTests'
            }
        }
           stage('stage-6 : install') {
             stepes {
                  sh 'mvn install -DskipTests'
        }
     }
         stage('Stage-7 : Verify') { 
            steps {
                sh 'mvn verify -DskipTests'
            }
        } 
     }
 }
 
