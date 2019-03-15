pipeline { 
    agent any 
    stages {
        stage('Build') { 
            steps { 
                sh 'echo build'
            }
        }
        stage('Run Tests') {
            parallel {
                stage('Unit Tests') {
                    agent any 
                    steps {
                        sh 'echo Unit Tests'
                    }
                }
                stage('Smoke Tests') {
                    agent any 
                    steps {
                        sh 'echo Smoke Tests'
                    }
                }
            }
        }
        stage('Artifact upload') {
            steps {
                sh 'echo test'
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo deploy'
            }
        }
    }
}
