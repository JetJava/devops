pipeline {
    agent any

    stages {
            stage('Prepare'){
                container('maven'){
                    steps{
                        sh 'printenv'
                    }
                }
            }
    }
}