pipeline {
  agent none 
   stages {
    stage('Hello') {
     steps {
        echo "hello from Jenkinsfile"
        }
     }
     stage('for the fix brach') {
        when {
          branch "fix-*"
        }
        steps {
          sh ''' 
          cat README.md 
          '''
        }
     }
     stage ('for the PR') {
        when {
          branch 'PR-*'
        }
        steps {
          echo 'this only runs for the PRs'
        }
     }
   }
}

