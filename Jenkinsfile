pipeline {
    agent any

    stages {
        stage("Build") {
            steps {
                sh 'echo "Buuild"'
            }
        }

        stage("SetUp"){
            steps{
                sh './script.sh'
            }   
        }
    }
}