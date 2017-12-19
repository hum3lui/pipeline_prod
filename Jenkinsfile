pipeline {
    agent any

    stages {
        stage('task1_sit') {
            steps {
                echo "SIT banner"
            }
        }
        stage('task2_sit') {         
            steps {
                //bat  "set path=%path%C:\\Program Files (x86)\\Java\\jdk1.8.0_151\\bin;"
				bat 'mkdir C:\\tempDirectorySIT'
            
            }
        }
        stage('task3_sit') {
            environment {
                PATH = "%path%;C:\\Windows\\SysWOW64;C:\\Program Files (x86)\\Java\\jdk1.8.0_151\\bin"
            }
            steps {
                bat 'javac helloWorld.java'
                bat 'java helloWorld'
            }
        }
    }

     post {
        success{
            echo 'mail sent'
        }
        failure {
            echo 'rollback process'
        }
        
    }
}