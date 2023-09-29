pipeline {
    agent any

    stages {
            stage('Prepare'){
                steps{
                    container('maven'){
                        sh 'printenv'
                    }
                }
            }
    }
}