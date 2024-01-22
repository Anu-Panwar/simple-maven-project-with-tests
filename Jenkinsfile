pipeline {
    agent any

    stages {
        stage('Clean Up'){
            steps {
                deleteDir()
            }
        }
         stage("Clone Repo"){
            steps {
                sh "git clone https://github.com/anupanwa1/simple-maven-project-with-tests.git"
            }
        }
        stage("Build"){
            steps {
                dir("simple-maven-project-with-tests") {
                    sh "mvn -Dmaven.test.failure.ignore=true clean package"
                }
            }
        }
        stage("Test"){
            steps {
                dir("simple-maven-project-with-tests") {
                    sh "echo Testing will be done here"
                }
            }
        }
    }
}
