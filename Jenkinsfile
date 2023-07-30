pipeline {
    
    agent none

    environment {
        COMPOSE_PROJECT_NAME = "${env.JOB_NAME}-${env.BUILD_ID}"
    }
    stages {
        stage('Echo') {

            agent {
                dockerfile {
                    // alwaysPull false
                    // image 'microsoft/dotnet:2.2-sdk'
                    // reuseNode false
                    args '-u root:root'
                }
            }

            steps {
                
                echo sh(script: 'env|sort', returnStdout: true)

            }

        }
 
    }
    post {

        always {
            node('master'){
                
                sh  '''
               
                '''
            }
        }
    }
}
