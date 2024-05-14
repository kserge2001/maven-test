pipeline{
    agent any 
    tools{
        maven 'M2_HOME'
        
    }

    stages{
        stage('Checkout'){
            steps{
                git branch: 'main', url: 'https://github.com/kserge2001/maven-test.git'
            }
        }
        stage ("Sonarqube scan") {
          steps{
          withSonarQubeEnv('sonar') {  
        sh 'mvn verify org.sonarsource.scanner.maven:sonar-maven-plugin:sonar -Dsonar.projectKey=kserge2001_maven-test'
                }
  
          }
        }
        stage("clean"){
            steps{
                sh 'mvn clean install package'
            }
        }
    }
}