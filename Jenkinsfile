pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    // Scripted block inside Declarative
                    if (env.BRANCH_NAME == 'main') {
                        echo "Running production build..."
                    } else {
                        echo "Running dev build..."
                    }
                }
            }
        }
        stage('Test') {
            steps {
                echo "Running tests..."
            }
        }
    }

    post {
        success {
            echo "✅ Build succeeded!"
        }
        failure {
            echo "❌ Build failed!"
        }
    }
}
// This Jenkinsfile demonstrates a Declarative Pipeline with a scripted block