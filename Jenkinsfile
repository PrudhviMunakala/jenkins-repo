pipeline {
    agent {
        node {
            label 'ROBOSHOP'
        }
    }
        stages {
                stage('build') {
                    steps {
                        echo "build"
                    }
                }
                stage('test') {
                    steps {
                        echo "test"
                    }
                }
                stage('deploy') {
                    steps {
                        echo "deploy"
                    }
                }
        
    }
    post {
            always {
                echo "This will always run"
            }
            success {
                echo "This will run only if successful"
            }
            failure {
                echo "This will run only if failed"
            }
        }
}