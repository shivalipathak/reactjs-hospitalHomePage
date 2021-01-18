pipeline {
  agent {  
  
  tools {nodejs "node"}
  
  stages {
    stage ("Install dependencies") {
      steps {
        echo 'Installing NPM packages'
        sh 'npm install'
      }
    }
    stage ("build") {
      steps {
        echo 'building the application'
        sh 'npm run build'
      }
    }
    stage ("deploy") {
      steps {
        echo 'deploying the application'
        sh 'docker'
      }
    }
  }
}
