pipeline {
  agent any
  stages {
    stage('Pull') {
      steps {
        git 'https://github.com/razer1259/mean.git'
      }
    }
    stage('List') {
      steps {
        sh '''echo $PWD
ls'''
      }
    }
    stage('Docker deploy') {
      steps {
        sh '''sudo apt-get install -y python-pip && sudo pip install docker-compose
docker-compose -f docker-compose-production.yml up -d'''
      }
    }
  }
}