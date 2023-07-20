pipeline{
    agent any

    tools {
         maven 'maven'
         jdk 'java'
    }

    stages{
        stage('checkout'){
            steps{
                checkout scmGit(branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: '3cbfc13d-c58e-4da2-948c-79944243798f', url: 'https://github.com/AradhanaDemo/java-hello-world-with-maven.git']])
        }
        stage('build'){
            steps{
               sh 'mvn package'
            }
        }
    }
}
