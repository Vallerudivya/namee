pipeline {
    agent any

    stages {
        stage('contineous download') {
            steps {
               git 'https://github.com/koddas/war-web-project.git'
            }
        }
         stage('contineous build') {
            steps {
               sh 'mvn install'
            }
        }
         stage('contineous deployment') {
            steps {
             sh 'sshpass -p "divya" scp target/wwp-1.0.0.war divya@172.17.0.2:/var/lib/apache-tomcat-9.0.56/webapps'
            }
        }
    }
}

