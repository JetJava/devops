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
                        script {
                            git branch: 'master',
                                credentialsId: 'github-ssh',
                                url: env.REPO
                        }
                        sh 'sleep 30'
                    }
                }
            }
    }
}