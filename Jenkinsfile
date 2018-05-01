pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }
        post {
            success {
                echo 'TNow Archiving...'
                archiveArtifacts artifacts: '**/target/*.war'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
