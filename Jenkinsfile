pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ -o hello task5.cpp'
            }
        }

        stage('Test') {
            steps {
                sh './hello'
            }
        }

        stage('Deploy') {
            steps {
                'deployed successfully'
            }
        }
    }

    post {
        always {
            script {
                if (currentBuild.result == 'FAILURE') {
                    echo 'pipeline failed'
                }
            }
        }
}
}
