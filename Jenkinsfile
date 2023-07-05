pipeline {
    agent any

    stages {
        stage('vcs') {
            steps {
                git branch: 'main', url: 'https://github.com/srikanth458hk/spring-petclinic.git'
            }
        }
        stage('build') {
            steps {
                sh 'mvn package'
            }
        }

    }
}    
