pipeline {
    agent any
    stages{
        stage("git clone") {
            steps {
                git branch: 'main', credentialsId: 'github13', url: 'https://github.com/venkat90107/prod.git'
            }
        }
    }
}
