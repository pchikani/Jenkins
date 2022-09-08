pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Checkout from GITHUB'
                git branch: 'main', changelog: false, credentialsId: '115456c2-7b9d-4909-96cf-a69c56e8b086', poll: false, url: 'https://github.com/pchikani/Jenkins.git'
                sleep 120 
            }
        }
        stage('Compile'){
            steps {
                echo 'Compile the checkout code'
                sh 'javac HelloJava.java'
                sleep 120
            }
        }
        stage('Execute'){
            steps {
                echo 'Execute the compiled java file'
                sh 'java HelloWorld'
                sleep 120
            }
        }
    }
}
