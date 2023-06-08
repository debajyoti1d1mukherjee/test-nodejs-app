pipeline { 
  
   agent any

   stages {
   
     stage('Install Dependencies') { 
       when {
        branch 'master'
      }
        steps { 
           sh 'echo "Install dependencies ..only for master"' 
        }
     }
     
     stage('Test') { 
       when {
           anyOf {
                    branch "dev"
                    branch "master"
                    branch "qa"
                    branch "stage"
                }
      }
        steps { 
           sh 'echo "testing application..."'
        }
      }

         stage("Deploy application") { 
         steps { 
           sh 'echo "deploying application..."'
         }

     }
  
   	}

   }
