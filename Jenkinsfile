pipeline {
    agent any
    
    stages {
        stage('Setup parameters') {
            steps {
                script { 
                    properties([
                        parameters([
                            choice(
                                choices: ['ONE', 'TWO'], 
                                name: 'Parameter'
                            )
                            
                        ])
                    ])
                }
            }
        }
        stage("Build") {
            steps {
                sh 'echo "$Parameter"'
            }
        }
    }
}