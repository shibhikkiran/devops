pipeline {
    agent any 
    
    stages {
    
        stage("run frontend") {
          
            steps {
                echo "executing yarn..." 
                nodejs('nodejs-10.17.0') {
                    sh 'yarn install'
                }
            }
        }

        stage("run backend") {
          
            steps {
                echo "executing gradle..." 
                withGradle() {
                    sh './gradlew -v'
                }
            }   
        }

        stage("deploy") {
          
            steps {
                echo "deploying the pipeline..."
            }   
        }
    }
}

