pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Checkout from GITHUB'
                git branch: 'main', changelog: false, credentialsId: 'xxxxxxx', poll: false, url: 'https://github.com/pchikani/Jenkins.git'
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
        stage('Finish'){
            steps {
                echo 'Last job in the pipeline to confirm completion'
                sh 'echo "Pipeline is complete"'
                sleep 120
            }
        }
    }
}
