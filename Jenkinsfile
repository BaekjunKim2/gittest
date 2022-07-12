pipeline {
  agent any
  stages {
    stage('Clone') {
      steps {
        git(poll: true, url: 'https://github.com/BaekjunKim2/gittest', branch: 'master', changelog: true)
      }
    }

    stage('Edit') {
      steps {
        sh 'echo \'echo\' > myfile'
      }
    }

    stage('Git') {
      steps {
        sh 'git config user.name "Jenkins"'
        sh 'git config user.email "jenkins@vuno.co"'
        sh 'git add -A'
        sh 'git commit -m "Jenkins commit"'
        sh 'git push'
      }
    }
  }
}
