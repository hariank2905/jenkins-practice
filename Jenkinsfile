pipeline {
     agent { node { label 'AGENT-1' } }

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh '''
                ls -ltr
                pwd
                
                '''
                echo 'This is from the git webhook'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
                // error 'This is failed'
            }
        }
    }

    post { 
        always { 
            echo 'I will always run whether job is succes or not'
        }
        success {
            echo 'i will run only the job is success'
        }
        failure {
            echo 'ill run if the job is failed'
        }
    }
}