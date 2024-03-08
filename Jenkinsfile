pipeline{
    agent any
    stages{
        stage('Build'){
            steps{
                build 'PES1UG21CS391-1'
                sh 'g++ prog.cpp -o output'
            }
        }
        stage('Test'){
            steps{
                sh './output'
            }

        }
        stage('Deploy'){
            steps{
                echo 'deploy'
            }
        }
    }
    post{
        failure{
            error 'Pipeline failed'
        }
    }
}