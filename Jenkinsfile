pipeline {
    agent any
    environment {
        ENV_URL= "pipeline.google.com"
    }
    stages {
        stage('stage one') {
            steps {
                sh '''
                echo 'Hello World'
                echo environment URL is ${ENV_URL}
                '''
            }
        }
        stage('Example Deploy') {
            when {
                branch 'production'
            }
            steps {
                echo 'Deploying'
            }
        }
    }
}