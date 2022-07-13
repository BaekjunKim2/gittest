pipeline {
  agent any
  stages {
    stage('Clone') {
      steps {
        git credentialsId: 'github-baekjun', poll: false, url: 'https://github.com/BaekjunKim2/gittest'
      }
    }

    stage('Edit') {
      steps {
        sh 'echo apple >> myfile'
      }
    }

    stage('Git') {
      steps {
        sh 'git config user.name "Jenkins"'
        sh 'git config user.email "jenkins@vuno.co"'
        sh 'git config push.default current'
        sh 'git commit -am "Jenkins commit"'
        sh 'git push'
      }
    }
  }
}
