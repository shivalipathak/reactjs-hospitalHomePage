pipeline {
  agent any 
  
  stages {
    stage ("Install dependencies") {
      steps {
        echo 'Installing NPM packages'
        sh 'npm'
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
        sh 'cp /usr/local/Cellar/erlang/23.2.1/lib/erlang/lib/inets-7.3.1/examples/server_root'
      }
    }
  }
}
