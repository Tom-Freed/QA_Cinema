pipeline {
    agent any
    // environment {
    //     SECRET_KEY=credentials('SECRET_KEY')
    // }
    stages {
        stage('Build') {
            steps {
                sh "sudo apt install -y python3-pip"
                sh "export SECRET_KEY=${SECRET_KEY}"
                sh "env"
            }
        }
        stage('Dependencies') {
            steps {
                sh "pip install -r requirements.txt"
            }
        }
        // stage('Testing') {
        //     steps {
        //         // add testing steps
        //     }
        // }
        stage('Deploy') {
            steps {
                sh "python3 app.py"
            }
        }
    }
}
// add environment config
// install dependencies
// add docker step to build containers from images...