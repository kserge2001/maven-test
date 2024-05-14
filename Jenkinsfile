pipeline{
    agent any 
    tools{
        maven 'M2_HOME'
    }

    stages{
        stage("clean"){
            steps{
                sh 'mvn clean install package'
            }
        }
    }
}