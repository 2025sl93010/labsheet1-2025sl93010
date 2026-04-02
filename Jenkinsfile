pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'YOUR_GITHUB_REPO_URL'
            }
        }

        stage('Build') {
            steps {
                sh 'echo "Build stage running"'
            }
        }

        stage('Test') {
            steps {
                sh '''
                python3 -c "
import calculator
assert calculator.add(2,3)==5
assert calculator.subtract(5,3)==2
assert calculator.multiply(2,3)==6
assert calculator.divide(6,3)==2
print('All tests passed')
"
                '''
            }
        }

        stage('Deploy') {
            steps {
                sh 'echo "Deploy stage placeholder"'
            }
        }
    }
}
