pipeline{
    agent any
    tools{
        maven 'Maven'
        jdk 'JDK9'
    }
    stages{
        stage("Build & SonarQube Analysis"){
            agent any
            steps{
                withSonarQubeEnv('sonar-server'){
                    bat 'java -version'
                    bat 'mvn clean package sonar:sonar'
                }
            }
        }
    }
}
