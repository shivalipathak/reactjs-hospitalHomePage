pipeline {
  agent any 
  
  stages {
    stage ("Install dependencies") {
      steps {
        echo 'Installing NPM packages'
        bash 'npm install'
      }
    }
    stage ("build") {
      steps {
        echo 'building the application'
        bash 'npm run build'
      }
    }
    stage ("deploy") {
      steps {
        echo 'deploying the application'
        bash 'cp /usr/local/Cellar/erlang/23.2.1/lib/erlang/lib/inets-7.3.1/examples/server_root'
      }
    }
  }
}
