pipeline {
    agent any

    stages {
        stage('Validate') {
            steps {
                sh 'mvn validate'
            }
        }
        stage('Compile') {
            steps {
                sh 'mvn compile'
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
        stage('package') {
            steps {
                sh 'mvn package'
            }
        }
        stage('install') {
            steps {
                sh 'mvn install' 
            }
        }
        stage('delivery'){
          steps {
          sh 'mvn deploy'
             }
        }
        stage('deploy') {
            steps {
                sh 'mvn tomcat7:undeploy tomcat7:deploy'
            }
        }

    }
}
