pipeline {
    agent any 
    
    stages {
    
        stage("build") {
          
            steps {
                echo "building the pipeline..." 
                script {
                    def test = 2 + 2 > 5 ? 'Cool' : 'Not So Cool'
                    echo test
                }
            }
        }

        stage("test") {
          
            steps {
                echo "testing the pipeline..." 
            }   
        }

        stage("deploy") {
          
            steps {
                echo "deploying the pipeline..."
            }   
        }
    }
}

