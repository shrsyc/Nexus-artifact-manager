pipeline{
    agent any
    tools{
        maven 'maven'
    }
    stages{
        stage('Build'){
            steps{
                sh 'mvn clean package'
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