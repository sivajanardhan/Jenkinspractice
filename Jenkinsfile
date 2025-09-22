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
                echo 'Hello World'
                sh mkdir  jp
                sh pwd 

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