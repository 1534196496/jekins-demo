pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out code from Bitbucket...'
            }
        }

        stage('Build') {
            steps {
                echo 'Building the project...'
            }
        }

        stage('Deploy to Environments') {
            when {
                branch 'master'
            }
            steps {
                def environments = ['stage-eu', 'stage-us', 'prod-eu', 'prod-us']

                parallelStages {
                    environments.each { environment ->
                        stage("Deploy to $environment") {
                            steps {
                                echo "Deploying to $environment..."
                            }
                        }
                    }
                }
            }
        }
    }
}
