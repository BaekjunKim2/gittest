pipeline {
  agent any
  stages {
    stage('Clone') {
      steps {
        git credentialsId: 'github-baekjun', poll: false, url: 'https://github.com/BaekjunKim2/gittest'
        sh 'git config user.email "jenkins@vuno.co"'
        sh 'git config user.name "jenkins"'
        sh 'echo apple >> myfile'
        sh 'git commit -am "Jenkins commit"'
        sh 'git push'
      }
    }
  }
}
