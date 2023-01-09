pipeline {
  agent {
    node {
      label 'windows'
    }

  }
  stages {
    stage('checkout Code') {
      steps {
        git(url: 'git@github.com:lidorg-dev/jenkins-ci-template.git', branch: 'master', poll: true, credentialsId: 'github-ssh')
      }
    }

    stage('build ') {
      steps {
        bat 'cd src\\MyWindowsService; nuget restore -source "https://api.nuget.org/v3/index.json"'
      }
    }

  }
}