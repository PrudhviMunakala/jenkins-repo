pipeline {
    agent {
        node {
            label 'roboshop-java-agent'
        }
    }
       parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')
        booleanParam(name: 'DEPLOY', defaultValue: true, description: 'Toggle this value')
        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')
        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
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
                        echo "${params.DEPLOY}"
                    }
                }
                stage('deploy') {
                     when {
                        expression { "${params.DEPLOY}" == "true" }
                    }
                    steps {
                       sh """
                            echo "deploy success"
                            
                          """
                    }
                }
        
    }
    // post {
    //         always {
    //             echo "This will always run"
    //         }
    //         success {
    //             echo "This will run only if successful"
    //         }
    //         failure {
    //             echo "This will run only if failed"
    //         }
    //     }
}