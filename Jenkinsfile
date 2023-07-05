pipeline {
    agent any

    stages {
        stage('vcs') {
            steps {
                git branch: 'main', url: 'https://github.com/saisrinisrinivas/spring-petclinic.git'
            }
        }
        stage('build') {
            steps {
                sh 'mvn package'
            }
        }

    }
}    
