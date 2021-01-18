pipeline {
  agent any
  
  tools {nodejs "node", docker "docker"}
  
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
