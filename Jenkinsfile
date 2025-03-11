pipeline{
    agent any
    tools{
        maven 'maven'
    }
    stages{
        stage('clean workspace'){
            steps{
                sh 'mvn clean'
            }
        }
        stage('validate code'){
            steps{
                sh 'mvn validate'
            }
        }
        stage('compile code'){
            steps{
                sh 'mvn compile'
            }
        }
        stage('test code'){
            steps{
                sh 'mvn test'
            }
        }
        stage('package code'){
            steps{
                sh 'mvn package'
            }
        }

        stage('store artifact in nexus'){
            steps{
                sh 'mvn -s Settings.xml clean deploy'
            }
            post{
                success{
                    echo 'Artifact stored in Nexus'
                }
                failure{
                    echo 'Failed to store artifact in Nexus'
                }
            }
        }
    }
}