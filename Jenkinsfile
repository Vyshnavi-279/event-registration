pipeline {
    agent any

    stages {

        stage('Verify Files') {
            steps {
                echo 'Checking project files...'

                sh 'test -f index.html'
                sh 'test -f reg.html'
                sh 'test -f style.css'

                echo 'All required files are present.'
            }
        }

        stage('Build') {
            steps {
                echo 'Building Event Registration Frontend...'

                sh 'echo "Frontend project build completed successfully."'
            }
        }

        stage('Test') {
            steps {
                echo 'Running basic tests...'

                sh 'test -s index.html'
                sh 'test -s reg.html'
                sh 'test -s style.css'

                echo 'All tests passed.'
            }
        }
    }

    post {
        success {
            echo 'SUCCESS: Event Registration project built successfully!'
        }

        failure {
            echo 'FAILURE: Please check the Jenkins console output.'
        }
    }
}
