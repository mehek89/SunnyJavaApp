pipeline {
    agent any

    tools {
        // Make sure Jenkins has JDK installed and configured
        jdk 'JDK21'
    }

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/mehek89/SunnyJavaApp.git'
            }
        }

        stage('Compile') {
            steps {
                sh 'javac src/Main.java -d .'
            }
        }

        stage('Run') {
            steps {
                sh 'java Main'
            }
        }
    }

    post {
        success {
            echo 'SunnyJavaApp ran successfully!'
        }
        failure {
            echo 'Something went wrong!'
        }
    }
}
