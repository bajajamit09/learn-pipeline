pipeline {
  agent {
    node {
      label 'master' 
    }
  }
  stages {
    stage('preamble') {
        steps {
            script {
                openshift.withCluster() {
                    openshift.withProject('jenkins') {
                        echo "Tesing Pipeline"
                    }
                }
            }
        }
    }
    stage('Build') {
      steps {
        script { 
          echo "Hello Poonam"
          sh 'mvn clean package'
        }
      }
    }
}    
}
