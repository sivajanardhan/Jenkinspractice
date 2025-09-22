pipeline {
    agent { node { label 'agent-1' } } 
    
    stages {
        stage('Example') {
            agent any
            options {
                // Timeout counter starts BEFORE agent is allocated
                timeout(time: 1, unit: 'SECONDS')
            }
            steps {
                sh '''
                sh 'echo 'Hello World'
                sh 'mkdir -p jp'
                sh 'echo "Hello World" > jp/hello.txt'
                sh 'cat jp/hello.txt'

                '''
            }
        }
    }
    post { 
        always { 
            echo 'I will always say Hello again!'
        }
    }


}