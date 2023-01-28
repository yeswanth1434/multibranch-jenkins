pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
        stage('git checkout') {
            when{
                branch 'feature'
            }
            steps {
                git branch: 'main', credentialsId: 'git-creds', url: 'https://github.com/yeswanth1434/multibranch-jenkins'
            }
        }
        stage('maven build') {
            when{
                branch 'devlop'
            }
            steps {
                sh"mvn clean package"
            }
        }
        stage('Tomcat Deploy - devlop') {
            when{
                branch 'devlop'
            }
            steps {
                echo "Deploying to devlop"
            } 
        }
        stage('Tomcat Deploy - prod') {
            when{
                branch 'main'
            }
            steps {
                echo "Deploying to production"
            }
        }
    }
}
