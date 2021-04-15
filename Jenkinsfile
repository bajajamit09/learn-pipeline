pipeline {
  agent {
    node {
      label 'maven' 
    }
  }
  stages {
    stage('preamble') {
        steps {
            script {
                openshift.withCluster() {
                    openshift.withProject('jenkins') {
                        echo "Tesing First Pipeline "
                    }
                }
            }
        }
    }
    stage('Build') {
      steps {
        script { 
          echo "Hello World"
          sh 'cd hello-java/app-src && mvn package' 
        }
      }
    }
}    
}
