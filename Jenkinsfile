pipeline {
      agent any

    stages {
        stage('Build') {
            steps {
                // Compile the .cpp file using a shell script
                sh 'g++ -o PES1UG21CS215-1 PES1UG21CS215.cpp'
            }
        }
        stage('Test') {
            steps {
                // Print output of .cpp file using a shell script
                sh './PES1UG21CS215-1'
            }
        }
        stage('Deploy') {
            steps {
                // Add deployment steps if applicable
                echo 'Deployment completed successfully'
            }
        }
    }

    post {
        always {
            echo 'Pipeline finished'
        }
        failure {
            echo 'Pipeline failed'
        }
    }
}
