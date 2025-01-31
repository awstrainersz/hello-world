pipeline {
    agent any
    environment{
        PATH ="/usr/share/apache-maven:$PATH"
    }
    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
        stage('Build stage ') {
            steps {
                git credentialsId: 'git-credential', url: 'https://github.com/awstrainersz/hello-world.git'
                sh 'mvn clean install'
            }
        }
    }
}
