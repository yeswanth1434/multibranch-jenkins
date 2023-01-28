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
            when{
                branch 'feature1'
            }
            steps {
                sh"mvn clean package"
            }
        }
    }
}
