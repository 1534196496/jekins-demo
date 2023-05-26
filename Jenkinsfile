pipeline {
  agent any
  stages {
    stage('error') {
      steps {
        sh '''echo "Environment Variables:"
echo ${env}'''
        input(message: 'who are you', id: 'id', ok: 'ok', submitter: 'Submitter', submitterParameter: 'SubmitterParameter')
      }
    }

  }
}