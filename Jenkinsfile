pipeline {
    agent any

    tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "M398"
    }

    stages {
        stage('Echo Version'){
            steps{
                sh 'echo Print Maven Version'
                sh 'mvn -version'
            }
            
        }
        
        stage('Build'){
            steps{
                git branch: 'main', url: 'http://139.84.159.194:555/dasher-org/jenkins-hello-world.git'
                
                sh "mvn clean package -DskipTests=true"
            }
        }    
        
        stage('Unit Test'){
            steps{
                sh "mvn test"
            }
        }
    
    
    }
}
