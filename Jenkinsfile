pipeline {
    agent {
        node {
            label 'roboshop-java-agent'
        }
    }
        stages {
                stage('build') {
                    steps {
                        sh """
                            echo "build success"
                            
                          """
                    }
                }
                stage('test') {
                    steps {
                        echo "test success"
                    }
                }
                stage('deploy') {
                    steps {
                        echo "deploy success"
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