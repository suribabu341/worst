pipeline {
    agent any

    stages {
        stage('cd') {
            steps {
                git '  https://github.com/Premvikash/java-maven-sample-war.git'
          }
        }
        stage('cb') {
            steps {
                 sh 'mvn install'
          }
        }
        stage('continuos deploy') {
            steps {
                sh 'sshpass -p "suri" scp target/Example-0.0.1-SNAPSHOT.war root@172.17.0.3:/opt/apache-tomcat-9.0.56/webapps'
          }
        }
    }
}

