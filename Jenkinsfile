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
        withCredentials([gitUsernamePassword(credentailsId: 'github-baekjun', gitToolName: 'git-tool')]) {
          sh 'git add myfile; git commit; git push'
        }
      }  
    }
  }
}
