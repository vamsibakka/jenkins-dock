pipeline {
  agent {label 'dock'}
  stages{
    stage ('clone') {
        steps {
            git branch:'master' , url : 'https://github.com/vamsibakka/jenkins-dock.git'
        }

    }
    stage ('image') {
        steps {
            sh 'docker image build -t test:1.0 .'
            sh 'docker container run -d --name conttest -P test:1.0'
        }
    }
  }
}