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
                        sh 'cd ' + env.WORKSPACE
                        sh 'ls -la'
                    }
                }
            }
            stage('Build'){
                steps{
                    container('maven'){
                        sh 'mvn clean package'
                        sh 'ls -la'
                        sh 'cd target'
                        sh 'ls -la'
                    }
                }
            }
    }
}