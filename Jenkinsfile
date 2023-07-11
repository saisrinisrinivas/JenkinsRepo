pipeline {
  agent any

  stages {
    
    stage('Fetch Scripts') {
      steps {
         checkout([$class: 'GitSCM', branches: [[name: '*/main']],
                    userRemoteConfigs: [[url: 'https://github.com/saisrinisrinivas/nodejsrepo.git']]])
        sh 'chmod +x build.sh push.sh deploy.sh'
      }
    }
                 }
    stage ('Build') {

      steps {
        sh './build.sh'
      }
    }
    stage ('Push') {

      steps {
        sh './push.sh'
      }
    }
    stage ('Deploy') {

      steps {
        sh './deploy.sh'
      }
    }
    
  }
}

    

    
    
  
