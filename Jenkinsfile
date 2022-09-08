pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Checkout from GITHUB'
                sleep 120 
            }
        }
        stage('Compile'){
            steps {
                echo 'Compile the checkout code'
                sleep 120
            }
        }
        stage('Execute'){
            steps {
                echo 'Execute the compiled java file'
                sleep 120
            }
        }
    }
}
