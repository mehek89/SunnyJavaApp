pipeline {
    agent any

    tools {
        jdk 'JDK21' // Make sure JDK is configured in Jenkins
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/mehek89/SunnyJavaApp.git'
            }
        }

        stage('Compile') {
            steps {
                bat 'javac src\\Main.java -d .'
            }
        }

        stage('Run') {
            steps {
                bat 'java Main'
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
