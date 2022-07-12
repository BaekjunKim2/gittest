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

  }
}