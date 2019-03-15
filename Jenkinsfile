pipeline { 
    agent any 
    stages {
        stage('Build') { 
            steps { 
                sh 'echo build'
            }
        }
        stage('Unit Tests') {
            steps {
                sh 'echo Unit Tests'
            }
        }
        stage('Upload Package') {
            steps {
                sh 'echo test'
            }
        }
        stage('Deploy to UAT') {
            steps {
                sh 'echo deploy'
            }
        }
        stage('Run Tests') {
            parallel {
                stage('Smoke Tests') {
                    agent any 
                    steps {
                        sh 'echo Smoke Tests'
                    }
                }
                stage('Regression Tests') {
                    agent any 
                    steps {
                        sh 'echo Regression Tests'
                    }
                }
            }
        }
    }
}
