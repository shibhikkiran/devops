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
                echo "executing maven..." 
                    def mavenHome = tool name: "maven-3.6.3", type: "maven"
                    def mavenCMD = "${mavenHome}/bin/mvn -v"
                    sh "${mavenCMD}"
            }   
        }

        stage("deploy") {
          
            steps {
                echo "deploying the pipeline..."
            }   
        }
    }
}

