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
            stage('Checkout'){
                steps{
                    container('maven'){
                        sh 'git clone ' + env.REPO
                        sh 'sleep 30'
                    }
                }
            }
    }
}