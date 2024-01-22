
pipeline {
    agent any

    tools {
       
        maven "m3"
    }

    stages {
         stage("Clean Up"){
            steps {
                deleteDir()
            }
        }
        stage("Build"){
            steps {
               
                    bat "mvn clean install"
                
            }
        }
    }
}
