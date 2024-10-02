pipeline {
    agent any

    stages{
        stage('SCM Checkout') {
            steps {
                echo 'Git clone the repo'
            }
        }
        
        stage('Install dependencies') {
            steps{
                echo 'Install requirements.txt'
            }
        }
        
        stage('Check for application functionality') {
            steps{
                echo 'Output from the multiplicaiton function'
                sh 'python3 -c "from calculator import multiply; print(multiply(100,50))"'
            }
        }

        stage('Unit Testing') {
            steps{
                echo 'Unit Testing started'
                sh 'python3 -m unittest discover'
            }
        }

        stage('Deploy Phase'){
            steps{
                echo 'Deploying application on ECR'
            }
        }
    }

}
