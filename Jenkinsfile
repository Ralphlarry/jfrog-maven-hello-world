pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
        stage('Its a great day!') {
            steps {
                echo 'Hello World, its indeed a great day'
            }
        }
        stage('Git checkout') {
            steps {
                checkout changelog: false, poll: false, scm: scmGit(branches: [[name: '*/DevOps']], extensions: [], userRemoteConfigs: [[credentialsId: 'My-Github-Login-Creds', url: 'https://github.com/Ralphlarry/jfrog-maven-hello-world.git']])
                sh 'ls -lrt'
                    }
                }
    }
}