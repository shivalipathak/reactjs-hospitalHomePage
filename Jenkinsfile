pipeline {
  agent any
  
  tools {nodejs "node"}
  
  def location = "https://github.com/shivalipathak/reactjs-hospitalHomePage.git"
  
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
    stage('Cloning Git') {
      steps {
        git 'https://github.com/shivalipathak/reactjs-hospitalHomePage.git'
      }
    }
    stage('Building image') {
      steps{
        script {
          dockerImage = docker.build "testdockerimage"
        }
      }
    }
    stage ("deploy") {
      steps {
        echo 'deploying the application'
        sh '/usr/local/bin/docker pull httpd'
        sh '/usr/local/bin/docker build -t reactjs-hospitalHomePage'
      }
    }
  }
}
