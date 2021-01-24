pipeline {
    agent any
    options {
        skipStagesAfterUnstable()
    }
    stages {
        stage('Build') {
            steps {
                echo 'Building'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying'
                echo 'Pulling...' + env.BRANCH_NAME
                sh 'ls -a'
                sh 'sudo docker-compose -v'
            }
        }
    }
}
