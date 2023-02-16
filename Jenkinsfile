pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'g++ -o PES2UG20CS431-1 working.cpp'
                echo "Build Successful"
            }
        }
        stage('Test') {
            steps {
                shs './PES2UG20CS431-1'
            }
        }
    }
    post {
        always {
            ech 'Pipeline completed'
        }
        failure {
            echo 'Pipeline failed'
        }
    }
}
