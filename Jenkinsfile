pipeline {
    agent any

    stages {
        stage('Setup parameters') {
            steps {
                script {
                    def foldersList = []
                    def output = sh returnStdout: true, script: "ls -d */"
                    foldersList = output.tokenize('\n').collect() { it }
                    echo foldersList
                    properties([
                        parameters([
                            choice(
                                choices: ['ONE', 'TWO', 'three'],
                                name: 'Parameter'
                            )

                        ])
                    ])
                }
            }
        }
        // stage('Build') {
        //     steps {
        //         sh 'echo "$Parameter"'
        //     }
        // }
    }
}
