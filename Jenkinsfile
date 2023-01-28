pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
        stage('git checkout') {
            steps {
                git branch: 'main', credentialsId: 'git-creds', url: 'https://github.com/yeswanth1434/multibranch-jenkins'
            }
        }
        stage('maven build') {
            steps {
                sh"mvn clean package"
            }
        }
        stage('Tomcat Deploy - devlop') {
            steps {
                echo "Deploying to devlop"
            } 
        }
        stage('Tomcat Deploy - prod') {
            steps {
                echo "Deploying to production"
            }
        }
    }
}
