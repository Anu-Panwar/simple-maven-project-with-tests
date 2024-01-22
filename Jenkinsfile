
pipeline {
    agent any

    tools {
       
        maven "m3"
    }

    stages {
        stage('Build') {
            steps {
                
                git 'https://github.com/anupanwa1/simple-maven-project-with-tests.git'

                dir('simple-maven-project-with-tests'){

                // Run Maven on a Unix agent.
                sh "mvn clean install"
                }

                // To run Maven on a Windows agent, use
                // bat "mvn -Dmaven.test.failure.ignore=true clean package"
            }
        }
    }
}
