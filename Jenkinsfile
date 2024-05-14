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
        stage("clean"){
            steps{
                sh 'mvn clean install package'
            }
        }
    }
}