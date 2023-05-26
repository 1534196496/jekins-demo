pipeline {
  agent any
  stages {
    stage('') {
      steps {
        sh ''' env.each { key, value ->
                        echo "${key}=${value}"
                    }'''
      }
    }

  }
}