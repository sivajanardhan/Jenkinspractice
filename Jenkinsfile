pipeline {
    agent { node { label 'agent-1' } } 
    
    stages {
        stage('Example') {
            agent any
            options {
                timeout(time: 1, unit: 'SECONDS')
            }

         
        stage('my-credentials') {
            environment { 
                AN_ACCESS_KEY = credentials('my-predefined-secret-text') 
            }
            steps {
                sh 'printenv'
            }
        }
    }
   


            steps {
                sh '''
                  echo "Hello World"
                  mkdir -p jp
                  echo "Hello World" > jp/hello.txt
                  cat jp/hello.txt
                '''
            }
        }
    }
    post { 
        always { 
            echo 'I will always say Hello again!'
        }

        success {
            echo 'I will say Hello only if the build succeeds!'
        }

        failure {
            echo 'I will say Hello only if the build fails!'
        }
    }



