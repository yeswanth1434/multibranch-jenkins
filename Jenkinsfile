pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
        stage('git checkout') {
<<<<<<< HEAD
            when{
                branch 'feature'
            }
=======
>>>>>>> 7b65ec8c6c2aa7bd5341d22c801354aacf8ac027
            steps {
                git branch: 'main', credentialsId: 'git-creds', url: 'https://github.com/yeswanth1434/multibranch-jenkins'
            }
        }
<<<<<<< HEAD
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
=======
>>>>>>> 7b65ec8c6c2aa7bd5341d22c801354aacf8ac027
    }
}
