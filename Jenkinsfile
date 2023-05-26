pipeline {
  agent any
  stages {
    stage('error') {
      steps {
        sh '''echo "Environment Variables:"
 withEnv(["PATH+JENKINS=${env.PATH}"]) {
                        sh \'echo $PATH+JENKINS\'
                    }'''
      }
    }

  }
}