pipeline {
    agent any

    stages {
        stage('contineous download') {
            steps {
               git 'https://github.com/Chandudhfp/DemoATC.git'
            }
        }
         stage('contineous build') {
            steps {
               sh 'mvn install'
            }
        }
        stage('contineous deploy') {
            steps {
               sh 'sshpass -p "chandu" scp target/DemoATR.war chandu@172.17.0.3:/opt/apache-tomcat-9.0.56/webapps'
            }
        }
        
    }
}

