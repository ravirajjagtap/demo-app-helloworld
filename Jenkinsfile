pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/ravirajjagtap/demo-app-helloworld.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'pip install -r requirements.txt || true'
            }
        }

        stage('Deploy Application') {
            steps {
                sh 'nohup python3 app.py > output.log 2>&1 &'
            }
        }
    }
}
