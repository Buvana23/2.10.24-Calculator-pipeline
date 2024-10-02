pipeline {
    agent any # jenkin master look and assign which is free

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
                sh 'python3 -m unittest discover' #will fetcht
            }
        }

        stage('Deploy Phase'){
            steps{
                echo 'Deploying application on ECR'
            }
        }
    }

}